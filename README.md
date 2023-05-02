Download Link: https://assignmentchef.com/product/solved-clc-project-4-pos-tagging
<br>



./viterbi.py input_hmm test_file output_file

I’m providing hmm.txt, which is in the following format (italics are replaced with values in the file):

state_num=<em>number of states </em>sym_num=<em>number of POS tags </em>

init

<em>tag P(tag | BOS) log10(P(tag | BOS)) </em>

<em>… </em>

transition<em> tag1 tag2 P(tag2 | tag1) log10(P(tag2 | tag1)) </em>

<em>… </em>

emission<em> tag word P(word | tag) log10(P(word | tag)) </em>

<em>… </em>

<ul>

 <li>If there is no transition probability from tag1 to tag2, then it is impossible to go from tag1 to tag2.</li>

 <li>If there is no transition probability from tag to word, then it is impossible for that tag to generate that word.</li>

</ul>

Each line of the test_file contains a single sentence.

The format of the output_file should be, one sentence per line: <em>word1</em>/<em>tag1 word2</em>/<em>tag2 word3</em>/<em>tag3…</em>