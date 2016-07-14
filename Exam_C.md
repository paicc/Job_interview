
This is C exam. it form [程式員面試寶典(第三版)](http://m.sanmin.com.tw/Product/Index/001680953) exam.

##C code
<ol>
####<li> Which of the following statement describe the results of executing the code snippet below in C?</li>

<pre><code>
int i = 1;
void main()
{
  int i = i;
}
</code></pre>

  <ol>
  <li>The i whithin main will have an undefined value</li>
  <li>The i within main wil have a value of 1</li>
  <li>The compiler will not allow this statement</li>
  <li>The i within main will have a value of 0</li>
  </ol>
---

####<li>what does the following program 'print'?</li>
<pre><code>
\#include <iostream>
using namespace std;
int main()
{
  int x=2,y,z;
  x *=(y=z=5); cout << x << endl;
  z=3;
  x ==(y=z); cout << x <<endl;
  x =(y==z); cout << x <<endl;
  x =(y&z); cout << x <<endl;
  x =(y&&z); cout << x << endl;
  y=4;
  x=(y|z); cout << x << endl;
  x=(y||z); cout << x << endl;
  return 0;
}
</cdoe></pre>
---

####<li>what does the following program 'print'?</li>
<pre><code>
#include <iostream>
using namespace std;
int func(int x)
{
  int count =0;
  while(x)
  {
    count ++;
    x=x&(x-1);
  }
  return count;
}

int main() {
  cout << func(9999) << endl;
  return 0;
}
</code></pre>
  <ol>
  <li>8</li>
  <li>9</li>
  <li>10</li>
  <li>11</li>
  </ol>

#####Note: while(x) == while (x != 0)

---

####<li>What is the difference of theese code?</li>

<ol>
<li>a code
<pre><code>
#include <iostream>
using namespace std;
int main()
{
  int a,x;
  for (a=0,x=0; a<=1 && !x++; a++)
  {
    a++;
  }
  cout << a << x << endl;
  return 0;
}
</code></pre>
</li>

<li> b code
<pre><code>
#include <iostream>
using namespace std;
int main()
{
  int a,x;
  for (a=0,x=0; a<=1 && !x++; )
  {
    a++;
  }
  cout << a << x << endl;
  return 0;
}
</code></pre>
</li>
</ol>

#####Note: for loop first round no ++

---

####<li> What will be the output of the following C code?</li>
<pre><code>
#include:stdio.h
main ()
{
	int b=3;
	int arr[]={6,7,8,9,10};
	sint *ptr=arr;
	*(ptr++)+=123;
	printf(" %d,%d\n", *ptr, *(++ptr));
}
</code></pre>

 <ol>
 <li>8 8</li>
 <li>130 8</li>
 <li>7 7</li>
 <li>7 8</li>
 </ol>

#####Note1: 'printf' calculated as the right-to-left 
	ex: 
	int a=8;
	printf("%d,%d",a,++a);
	answer is 9 9
#####Note2: \*(ptr++)+=123 => \*ptr=\*ptr+123; ptr++;
---

####<li>Which one is better?</li>
	//a is a veriable
<ol>
<li>A code
 <pre><code>
	if ('A'==a) {
		a++;
	}
</code></pre></li>
<li>B code
 <pre><code>
	if (a=='A') {
		a++;
	}
</code></pre></li>
</ol>

---
####<li>what this answer?</li>
	#include <iostream>
	#include <stdio.h>
	#include <string.h>
	#include <conio.h>
	using namespace std;
	int main()
	{
		float a = 1.0f;
		cout << (int)a << end;
		cout << &a << endl;
		cout << (int&)a << endl;
		cout << boolalpha << ( (int)a == (int&)a ) << endl; //output WHAT?
		
		float b = 0.0f;
		cout << (int)b << endl;
		cout << &b << endl;
		cout << (int&)b << endl;
		cout << boolalpha << ( (int)b == (int&)b ) << endl; //output WHAT?
		
		return 0;
	}

---
####<li> what this answer?</li>
	#include <stdio.h>
	
	int main()
	{
		unsigned int a =0xFFFFFFF7;
		unsigned char i = (unsigned char)a;
		char* b = (char*)&a;

		printf("%08x, %08x", i, *b);
	}

#####Note:
 <ol>
##### <li> Operator '&' used to get the address of the object</li>
	p= &c; //C's address copy to P , p pointer to c
##### <li> '*' is indirection
	int x = 1, y = 2, z[10];
	int *ip; 	/* ip is a pointer to int */
	ip = &x;	/* ip now points to x */
	y = *ip;	/* y is 1 */
	*ip = 0;	/* x is now 0 */:-1
	ip = &z[0]	/* ip now points to z[0] */
