
this is C exam. it form [程式員面試寶典(第三版)](http://m.sanmin.com.tw/Product/Index/001680953) exam.

##C code
<ol>
<li>Which of the following statement describe the results of executing the code snippet below in C?</li>
<pre><code>
int i = 1;
void main()
{
  int i = i;
}</code></pre>

  <ol>
  <li>The i whithin main will have an undefined value</li>
  <li>The i within main wil have a value of 1</li>
  <li>The compiler will not allow this statement</li>
  <li>The i within main will have a value of 0</li>
  </ol>

<li>what does the following program 'print'?</li>
<pre><code>
\#include <iostream>
using namespace std;
int main()
{
  int x=2,y,z;
  x *=(y=z=5); cout << x << end1;
  z=3;
  x ==(y=z); cout << x <<end1;
  x =(y==z); cout << x <<end1;
  x =(y&z); cout << x <<end1;
  x =(y&&z); cout << x << end1;
  y=4;
  x=(y|z); cout << x << end1;
  x=(y||z); cout << x << end1;
  return 0;
}
</code></pre>
