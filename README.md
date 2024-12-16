<h1><em><strong>What is scatter matrix</strong></em></h1>

<img src="2.png" alt="scatter matrix"/>

<p> <strong>Scatter Matrix</strong> is a data visualization tool that shows the relationships between numerical variables in the form of a set of scatter plots. </p>


<h3><em><strong>Scatter matrix structure</strong></em></h3>

<ul>
<li><em>Axis</em>
<br>
<p>Each column of data is plotted in pairs with other columns.</p>
</li>

<li><em>Main diameter</em>
<br>
<p>It usually displays the histogram or density of each feature (column).</p>
</li>

<li><em>Outside the main diameter</em>
<br>
<p>nemodar parakandegi bin npar do vijegi (do seton adadi) rasm mishod.
<br>A scatter plot is drawn between both features (two numerical columns).</p>
</li>
</ul>




<h3><em><strong>Why useful is</strong></em></h3>

<ol>
<li><em>1- Check Scatter Matrix:</em>
<br>
<p>Relation for linear or non-linear shows between variable</p>
</li>

<li><em>2- Class Separation:</em>
<br>
<p>Other points (Based on color) can be shows diferent between classifications(lables)</p>
</li>

<li><em>3- Data Distribution:</em>
<br>
<p>Through a histogram on the main diameter, the distribution of each variable is accessible</p>
</li>
</ol>


<h3><em><strong>How to run</strong></em></h3>
<p>in this example for scatter matrix use of simple fruits sorting data</p>

<ol>
<li><em>import the required library:</em>
<br>
<p>import pandas as pd
<br>
from pandas.plotting import scatter_matrix
<br>
from matplotlib import cm
<br>
</p>
</li>

<li><em>read file</em>
<br>
<p>
data=pd.read_table("fruits.txt")
<br>
<strong>description:</strong> The reason for using the read_table method in the pandas library is that our data set is a txt file containing tables
</p>
<img src="1.png" alt="read_table"/>
</li>

<li><em>division of x and y data:</em>
<br>
<p>features_name = ['mass','width','height','color_score']
<br>
x=data[features_name]
<br>
y=data["fruits_lable"]
<br>
</p>
</li>

<li><em>create a scatter matrix: </em>
<br>
<p>sc_matrx=scatter_matrix(x,c=y,marker='o',s=40,hist_kwds={'bind':15}, fig_size=(9,9), cmap=cmap)

<br>
<strong>descriptions:</strong>
<p>
arguments for scatter matrix
<br>
<strong>x</strong>: input data
<br>
<strong>c=y</strong>: any dot color with use of classification(lable) determind fruits
<br>
<strong>marker='o'</strong>: indicator type (marker) for data points
<br>
<strong>s=40</strong>: size data points
<br>
<strong>hist_kwds={'bins':15}</strong> : count of bin in histogram on main diameter
<br>
<strong>fig_size=(9,9)</strong>: size of diagram (w,h) to inch
<br>
<strong>cmap=cmap</strong>: use of selected color map for specifies scatter matrix color point
</p>
</li>

<li><em>define a cmap plan: </em>
<br>
<p>cmap=cm.getcmap("gnuplot")
</p>
</li>

</ol>