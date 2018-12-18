## Généralités
Termith-java est une chaîne de traitement qui permet de réaliser deux traitements en lien avec le projet termITH : 
- une procédure d'enrichissement sur des fichier au format pivot qui les enrichis de quatres couches d'annotations : 
    - une couche morpho-syntaxique 
    - une couche terminologique 
    - une couche phraséologique 
    - une couche transdisciplinaire 

- une procédure de désambiguisation qui permet, à l'aide d'un apprentissage préalable (avec un corpus annoté manuellement), de désambiguiser terminologiqument un corpus d'évaluation.  
## Dépendances
- java 8 (les dépendance sont dans le `.gradle`)
- R
- TreeTagger

- Termith-ressource
## I/O
### Pour le module d'enrichissement
- Entrée : des fichiers au [format pivot](TermITH/stdfSpec.md) sans couche d'annotation
- Sorties : des fichiers au [format pivot](TermITH/stdfSpec.md) avec couche d'annotation au format standOff

### Pour le module de désambiguisation
- Entrée : 
    - des fichiers au [format pivot](TermITH/stdfSpec.md) enrichis avec un éléments standOff de type 'candidatsTermes' annotés manuellement pour le corpus d'apprentissage :
        ```xml
      <ns:standOff type="candidatsTermes">
        <teiHeader>
          <fileDesc>
            <titleStmt>
              <title/>
            </titleStmt>
            <publicationStmt>
              <publisher/>
            </publicationStmt>
            <sourceDesc>
              <p/>
            </sourceDesc>
          </fileDesc>
        </teiHeader>
        <ns:listAnnotation>
         <!-- les élément span correspondent au occurrence de terme extraite.
         L'attribut target correspond au tokens du texte qui compose cette occurrence de terme.
         L'attribut corresp correspond à l'id d'une entrée terminologique présente dans la terminologie
         généré par la chaîne de traitements.
         l'attribut ana a pour valeur l'ensemble des annotations lié à ce termes -->
               <interpGrp>
            <interp xml:id="DM1">Occurrence du candidat terme validée seulement au niveau syntaxique</interp>
            <interp xml:id="DM2">Occurrence du candidat terme validée au niveau scientifique et syntaxique</interp>
            <interp xml:id="DM3">Occurrence du candidat terme validée au niveau disciplinaire, scientifique et syntaxique</interp>
            <interp xml:id="DM4">Occurrence du candidat terme validée sur tous les niveaux d'annotation. Elle est validée au niveau terminologique</interp>
            <interp xml:id="DM0">Occurrence du candidat terme rejetée dès le niveau syntaxique</interp>
          </interpGrp>
          <interpGrp>
            <interp xml:id="DAOn">Occurrence du candidat terme validée au niveau terminologique selon le système de désambiguïsation utilisé</interp>
            <interp xml:id="DAOff">Occurrence du candidat terme non valide par le système de désambiguïsation</interp>
          </interpGrp>
          <span target="#t2" corresp="#TS2.0-entry-5082" ana="#DM3">
            <fs>
              <f name="inflexionWord">
                <string>moulage</string>
              </f>
            </fs>
          </span>
          <span target="#t5" corresp="#TS2.0-entry-5991" ana="#DM1">
            <fs>
              <f name="inflexionWord">
                <string>stèle</string>
              </f>
            </fs>
          </span>
        </ns:listAnnotation>
      </ns:standOff>
       ``` 
    - des fichiers au [format pivot](TermITH/stdfSpec.md) enrichis avec un éléments standOff de type 'candidatsTermes' pour le corpus d'évaluation :
        ```xml
      <ns:standOff type="candidatsTermes">
        <teiHeader>
          <fileDesc>
            <titleStmt>
              <title/>
            </titleStmt>
            <publicationStmt>
              <publisher/>
            </publicationStmt>
            <sourceDesc>
              <p/>
            </sourceDesc>
          </fileDesc>
        </teiHeader>
        <ns:listAnnotation>
         <!-- les élément span correspondent au occurrence de terme extraite.
         L'attribut target correspond au tokens du texte qui compose cette occurrence de terme.
         L'attribut corresp correspond à l'id d'une entrée terminologique présente dans la terminologie
         généré par la chaîne de traitements.
         l'attribut ana a pour valeur l'ensemble des annotations lié à ce termes -->
               <interpGrp>
            <interp xml:id="DM1">Occurrence du candidat terme validée seulement au niveau syntaxique</interp>
            <interp xml:id="DM2">Occurrence du candidat terme validée au niveau scientifique et syntaxique</interp>
            <interp xml:id="DM3">Occurrence du candidat terme validée au niveau disciplinaire, scientifique et syntaxique</interp>
            <interp xml:id="DM4">Occurrence du candidat terme validée sur tous les niveaux d'annotation. Elle est validée au niveau terminologique</interp>
            <interp xml:id="DM0">Occurrence du candidat terme rejetée dès le niveau syntaxique</interp>
          </interpGrp>
          <interpGrp>
            <interp xml:id="DAOn">Occurrence du candidat terme validée au niveau terminologique selon le système de désambiguïsation utilisé</interp>
            <interp xml:id="DAOff">Occurrence du candidat terme non valide par le système de désambiguïsation</interp>
          </interpGrp>
          <span target="#t2" corresp="#TS2.0-entry-5082">
            <fs>
              <f name="inflexionWord">
                <string>moulage</string>
              </f>
            </fs>
          </span>
          <span target="#t5" corresp="#TS2.0-entry-5991">
            <fs>
              <f name="inflexionWord">
                <string>stèle</string>
              </f>
            </fs>
          </span>
        </ns:listAnnotation>
      </ns:standOff>
       ``` 
- Sorties : des fichiers au [format pivot](TermITH/stdfSpec.md) avec couche d'annotation au format standOff annoté automatiquement :
    ```xml
  <!-- un exemple d'extraction terminologique -->
      <ns:standOff type="candidatsTermes">
        <teiHeader>
          <fileDesc>
            <titleStmt>
              <title/>
            </titleStmt>
            <publicationStmt>
              <publisher/>
            </publicationStmt>
            <sourceDesc>
              <p/>
            </sourceDesc>
          </fileDesc>
        </teiHeader>
        <ns:listAnnotation>
                   <interpGrp>
            <interp xml:id="DM1">Occurrence du candidat terme validée seulement au niveau syntaxique</interp>
            <interp xml:id="DM2">Occurrence du candidat terme validée au niveau scientifique et syntaxique</interp>
            <interp xml:id="DM3">Occurrence du candidat terme validée au niveau disciplinaire, scientifique et syntaxique</interp>
            <interp xml:id="DM4">Occurrence du candidat terme validée sur tous les niveaux d'annotation. Elle est validée au niveau terminologique</interp>
            <interp xml:id="DM0">Occurrence du candidat terme rejetée dès le niveau syntaxique</interp>
          </interpGrp>
          <interpGrp>
            <interp xml:id="DAOn">Occurrence du candidat terme validée au niveau terminologique selon le système de désambiguïsation utilisé</interp>
            <interp xml:id="DAOff">Occurrence du candidat terme non valide par le système de désambiguïsation</interp>
          </interpGrp>
         <!-- les élément span correspondent au occurrence de terme extraite.
         L'attribut target correspond au tokens du texte qui compose cette occurrence de terme.
         L'attribut corresp correspond à l'id d'une entrée terminologique présente dans la terminologie
         généré par la chaîne de traitements.
         l'attribut ana a pour valeur l'ensemble des annotations lié à ce termes -->
          <span target="#t2" corresp="#TS2.0-entry-5082" ana="#DM3 #DAOff">
            <fs>
              <f name="inflexionWord">
                <string>moulage</string>
              </f>
            </fs>
          </span>
          <span target="#t5" corresp="#TS2.0-entry-5991" ana ="#DM1 #DAOn">
            <fs>
              <f name="inflexionWord">
                <string>stèle</string>
              </f>
            </fs>
          </span>
        </ns:listAnnotation>
      </ns:standOff>
     ```
     ## Pour en savoir plus
     Il y a un [README.md](https://git.atilf.fr/termith/termith-java/blob/develop/README.md) dans le projet contenant l'ensemble des informations néccéssaires pour éxécuter le docker ainsi que les arguments permettant de spécifier le corpus d'apprentissage et d'évaluation
     ## Liens vers le projet
     [https://git.atilf.fr/termith/termith-java](https://git.atilf.fr/termith/termith-java)