
This is C exam. it form [程式員面試寶典(第三版)](http://m.sanmin.com.tw/Product/Index/001680953) exam.
##C code

---

<ol>
<li> Which of the following statement describe the results of executing the code snippet below in C?</li>

	int i = 1;
	void main()
	{
		int i = i;
	}
<ol>
<li>The i whithin main will have an undefined value</li>
<li>The i within main wil have a value of 1</li>
<li>The compiler will not allow this statement</li>
<li>The i within main will have a value of 0</li>
</ol>

---

####<li>what does the following program `print`?</li>

	#include <iostream>
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

---

####<li>what does the following program `print`?</li>

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

#####Note: `for` loop first round no ++

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
#<li> *What this answer? </li>
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
<li> Operator `&` used to get the address of the object</li>
<pre><code>
	p= &c; //C's address copy to P , p pointer to c
</code></pre>
<li> `*` is indirection</li>
<pre><code>
	int x = 1, y = 2, z[10];
	int *ip; 	/* ip is a pointer to int */
	ip = &x;	/* ip now points to x */
	y = *ip;	/* y is 1 */
	*ip = 0;	/* x is now 0 */:-1
	ip = &z[0]	/* ip now points to z[0] */
</code></pre>
<li> </li>
<pre><code>
	unsigned int *a;
	char *b = (char *)&a;
	
	same as
	unsigned int *p = &a;	//p的內容為a的位址，即p指向a
	char *b = (char *)p;	//此處的強制轉換只是使b也指向a
</code></pre>
</ol>

---
####<li>Note: C++ knowledge</li>
<ol>
<li>Arithmetic Conversion</li>
<pre><code>
	int ival = 3;
	double dval = 3.14159;

	ival + dval;	//ival change to double:3.0
</code></pre>
<li> </li>
<pre><code>
	int ival;
	float fval;
	double dval;
	//進行運算前ival和fval都被轉換為double型態
	dval = dval + fval + ival;	
</code></pre>
</ol>

---

####<li>What is the answer?</li>
	#include <iostream>
	using namespace std;

	int main()
	{
		unsigned char a=0xA5;
		unsigned char b=~a>>4+1;
		
		printf("b=%d\n", b);
		return 0;
	}
<ol>
	1. 245</br>
	2. 246</br>
	3. 250</br>
	4. 2</br>
</ol>

#####Note:
1. ![C運算子優先權](https://sites.google.com/site/zsgititit/_/rsrc/1459904064687/home/c-cheng-shi-she-ji/ch2bian-shu-yu-yun-suan-zi/ch2%E8%AE%8A%E6%95%B8%E9%81%8B%E7%AE%97%E5%AD%90-001.jpg "C運算子優先權")
2. eax暫存器為16bit，所以，0xA5 = 0000 0000 1010 0101

---
####<li> 利用一個算式，判斷數字X是否為2的N次方，不可使用循環語句</li>
2 = 10</br>
4 = 100</br>
8 = 1000</br>
16 = 10000</br>
所以，如果X-1後與X做AND運算，答案若為0，則X為2的N次方

---
####<li> (729,271)=_____</li>
	int f(int x, int y)
	{
		return(x&y)+((x^y)>>1)
	}

---
####<li> There are two int variables: a and b, don't use `if`,`?:`,`switch` or other judgement statements, find out the biggest one of the two numbers.</li>
	int max = ((a+b) + abs(a-b)) / 2
#####Note: abs function 作用為取絕對值

---
####<li>將A.b兩個值進行交換，而不使用任何變數</li>
	a = a^b;
	b = a^b;
	a = a^b;
#####Note：NOR(^) => 相同為0 相異為1
---

####<li>在C++程式中呼叫被C Compiler所編譯後的函數，為何需要加extern "C"?</li>
	因為C++編譯後在library中的名字與C語言不同。
	C++語言支援函數重載，C語言不支援函數重載。
	所以，C++提供了C連接交換指定符號 extern "C"解決名字匹配問題

---

####<li>


 
