# DNAme


<script src="{{< blogdown/postref >}}index_files/header-attrs/header-attrs.js"></script>


<div id="what-is-dname" class="section level2">
<h2>What is DNAme?</h2>
<p>DNAme is an application for teaching/learning purposes which converts a word to a DNA sequence. It has some theory to understand the processes underlying this conversion, but this theroy must not be used with teaching puroposes because it may have some inaccuracies.</p>
</div>
<div id="how-dname-works" class="section level2">
<h2>How DNAme works?</h2>
<div id="summary" class="section level3">
<h3>Summary</h3>
<p>DNAme was designed using R/Shiny that takes your name as a sequence of one-letter aminoacids and converts them to DNA/mRNA by looking for the codon that codes for each aminoacid.</p>
</div>
<div id="one-letter-code-for-aminoacids" class="section level3">
<h3>One-letter code for aminoacids</h3>
<p>Since most aminoacids are coded by more than one codon, it takes the codon usage of several species into account, selecting the most frequent codon based on <a href="https://www.genscript.com/">genescript</a>’s <a href="https://www.genscript.com/tools/codon-frequency-table">codon frequency tables</a>. Currently the available organisms are human and mouse, but the idea is to have some of the most used model organisms (i.e. <em>A. thaliana</em>, <em>D. melanogaster</em>, <em>E. coli</em>, …).</p>
</div>
<div id="not-all-names" class="section level3">
<h3>Not all names</h3>
<p>It has to be taken into account that not all names can be converted to DNA/mRNA, because not all letters have an associated aminoacid. Hence, if a letter in your name is not possible, DNAme will throw an error message. You have two possibilites:</p>
<ul>
<li>Choose another word, such as a nickname or a surname.</li>
<li>Play with phonetics. For example, if your name contains an <em>X</em> you could change it by a combination of letters with a similar sound like <em>KS</em>, which are <em>Lysine</em> and <em>Serine</em>.</li>
</ul>
</div>
<div id="parameters" class="section level3">
<h3>Parameters</h3>
<p><em>DNAme</em> allows to select diverse parameters:</p>
<ul>
<li>Nucleic acid: DNA or mRNA</li>
<li>Organism (for the codon usage): Human or Mouse</li>
<li>Separator: character to separate the codons (i.e. a dash, a blank space, nothing).</li>
<li><em>in the future</em> Use extra letters.</li>
</ul>
</div>
</div>
<div id="availability" class="section level2">
<h2>Availability</h2>
<p><em>DNAme</em> is available <a href="https://biobit.netlify.app/dname.html">here</a> as a working application. This version is deployed to shinyapps.io and only one person at a time can be connected to the app.</p>
<p>To download the source code, go to the <a href="https://github.com/amitjavilaventura/DNAme">Github repository</a> and clone it. Then open R or RStudio, go to the <em>DNAme</em> directory (with <code>setwd()</code>) and run <code>shiny::runApp("app.R")</code> in the R console. In this case you will need to install some R packages:</p>
<ul>
<li><code>shiny</code></li>
<li><code>dplyr</code></li>
<li><code>magrittr</code></li>
<li><code>stringr</code></li>
</ul>
<p>In the future, I want to build it as a Desktop app using <code>photon</code>, but at the moment, this option is not available.</p>
</div>

