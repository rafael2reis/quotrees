# QuoTrees 1.0
The first corpus in Portuguese fully annotated with direct and indirect quotations

## Descriptive Statistics

The dataset has 460,966 tokens, 24,139 sentences, 5,199 feeds and 1,663 quotations. Table \ref{tab:count_rules} shows the distribution of quotations by type. We divide the counting in _quotations with subject_ and _quotations without subject_, the later being the sentences with missing subject.

<table>
  <tr>
    <td>Quotations' Type</td><td colspan=5>Direct</td><td>Indirect</td>
  </tr>
  <tr>
    <td>Rule</td><td>1</td><td>2</td><td>4</td><td>5</td><td>Total</td><td>3</td>
  </tr>
  <tr>
    <td># SUBJ</td><td>513</td><td>2</td><td>0</td><td>18</td><td>533</td><td>804</td>
  </tr>
  <tr>
    <td># Without SUBJ</td><td>117</td><td>1</td><td>0</td><td>0</td><td>118</td><td>208</td>
  </tr>
</table>

## Description

The Machine Learning approach is based on the assumption that a computer is able to learn through examples. In order to build an artificial intelligence that identifies quotations, we need to feed it with a large amount of examples of quotations. For this purpose, we built _QuoTrees 1.0_ and make it public available.

Corpus annotation is a recognized time-consuming task. A common way of optimizing this process is to combine automatic annotation with a second round of human revision. This is the strategy we follow.

Instead of building a corpus from a raw text, we use two public datasets that are already tokenized and annotated with linguistic labels: _Bosque, v.8_  and _Floresta Virgem_. Both are part of the _Floresta Sintá(c)tica_ project, created and maintained by [Linguateca](https://www.linguateca.pt/). Although the sources are the same, the sentences in _Bosque_ and _Floresta Virgem_ are unique to each. _Bosque_ is a subset of _Floresta Virgem_, fully revised and corrected by linguists with a current size of 9,368 sentences. _Floresta Virgem_ is a set of trees automatically created from the output of the PALAVRAS parser, corresponding roughly to the first million tokens of the CETEMPúblico and CETENFolha corpora. These corpora are made of extracts of news items from Público and Folha de São Paulo newspapers.

We use these datasets in the _AD_ (Árvores Deitadas - _phrase structure tree_) format, which is easier for human revision. We used only the first 37,386 sentences of _Floresta Virgem_, an amount feasible to be manually revised without compromising the automatic learning process/algorithm.

_QuoTrees 1.0_ is composed of several _feeds_. A _feed_ is a group of sentences from the same news item.

In order to build _QuoTrees 1.0_, we added information regarding the speech verb, the sayer and the content. This information came from SaburiFreitas2017, which identifies eight syntactic patterns in which reported speech verbs are commonly found in Portuguese.
