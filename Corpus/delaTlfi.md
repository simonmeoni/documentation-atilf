## Merge Tlfi-Dela

le fichier merge.xml est un fichier contenant les entrées phrasélogiques du Tlfi et du Dela au format tei (il ne contient pas encore de teiHeader et il reste quelques autres problèmes de format). Les entrées ayant une forme orthographique similaire ont été fusionnées.

il y a 3 types d'entrées :

1. Les entrées du TLF reformatées :
```
<entry source="#TLF_16304" type="reformat">
  <form>
    <form type="normalized" source="#TLF_16304">
      <orth>du bon Dieu</orth>
      <gramGrp>
        <gram type="contiguity">contiguous</gram>
      </gramGrp>
    </form>
  </form>
  <sense source="#TLF_16304">
    <def>(Subst.) propre aux êtres naïvement et entièrement voués à Dieu.</def>
  </sense>
</entry>
<entry source="#TLF_42615" type="reformat">
  <form>
    <form type="normalized" source="#TLF_42615">
      <orth>à ras de</orth>
      <gramGrp>
        <gram type="contiguity">contiguous</gram>
      </gramGrp>
    </form>
    <form type="normalized" source="#TLF_42615">
      <orth>au ras de</orth>
      <gramGrp>
        <gram type="contiguity">contiguous</gram>
      </gramGrp>
    </form>
  </form>
  <sense source="#TLF_42615">
    <def>Au niveau de.</def>
  </sense>
</entry>
```
2. Les entrée du DELA reformatées :

```
<entry source="#DELA_201271" type="reformat">
  <form>
    <form type="lemma" source="#DELA_201271">
      <orth>zooxanthelle symbiotique</orth>
    </form>
    <form type="inlflected" source="#DELA_201271">
      <orth>zooxanthelle symbiotique</orth>
      <gramGrp>
        <gram type="compound_pos">noun</gram>
        <gram type="gender">feminine</gram>
        <gram type="number">singular</gram>
      </gramGrp>
    </form>
  </form>
  <sense source="#DELA_201271">
    <usg type="subcat" source="#DELA_201271">concret</usg>
  </sense>
</entry>
```
3. Les entrée du DELA/Tlfi fusionnées :

```
<entry source="#TLF_20877 #DELA_148" type="merge_reformat">
  <form>
    <form type="lemma" source="#DELA_148">
      <orth>abcès de fixation</orth>
    </form>
    <form type="normalized" source="#TLF_20877">
      <orth>abcès de fixation</orth>
      <gramGrp>
        <gram type="contiguity">contiguous</gram>
      </gramGrp>
    </form>
    <form type="inflected" source="#DELA_148">
      <orth>abcès de fixation</orth>
      <gramGrp>
        <gram type="compound_pos">noun</gram>
        <gram type="gender">masculine</gram>
        <gram type="number">plural</gram>
      </gramGrp>
    </form>
  </form>
  <sense source="#TLF_20877">
    <def>Abcès artificiel où s'opère la localisation du pus.</def>
    <usg norm="médecine" type="dom">MÉD.</usg>
  </sense>
  <sense source="#DELA_148">
    <usg type="subcat">concret</usg>
  </sense>
</entry>
```

- l'élement `entry` est une entrée. L'attribut `source` a pour valeur l'identifiant appartenant au Tlfi ou au Dela. L'attribut `type` a deux valeurs possibles : reformat ou merge_reformat.
La valeur reformat est utilisée lorsque que l'entrée extraite a été reformatée au format du fichier merge.xml tandis que la valeur merge_reformat est utilisée lorsque l'entrée est issue à la fois du Tfli et du Dela (elle est aussi reformatée).
- l'élément `form` fils de `entry` contient les variantes orthographique de l'entrée concernée.
- les éléments `form` parent de `form` peuvent contenir l'élément `gramGrp` contenant les informations morpho-syntaxique du DELA ou du TLFi.
- l'élément `sense` contient les différentes informations sémantiques propres à une entrée du dictionnaire.

## Lien vers le projet
[https://git.atilf.fr/corpus/dela-tlfi](https://git.atilf.fr/corpus/dela-tlfi)