
This is C exam. it form [程式員面試寶典(第三版)](http://m.sanmin.com.tw/Product/Index/001680953) exam.

##C code

1. Which of the following statement describe the results of executing the code snippet below in C?
<pre><code>
int i = 1;
void main()
{
  int i = i;
}
</code></pre>

  
  1. The i whithin main will have an undefined value
  2. The i within main wil have a value of 1
  3. The compiler will not allow this statement
  4. The i within main will have a value of 0

2. what does the following program 'print'?
```cpp
#include <iostream>
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
```

3. what does the following program 'print'?
```cpp
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
  cout << func(9999) << end1;
  return 0;
}
```
  1. 8
  2. 9
  3. 10
  4. 11

**note:** while(x) == while (x != 0)

4. 


