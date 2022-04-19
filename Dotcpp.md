# 1000: [竞赛入门] 简单的a+b
```c
#include<stdio.h>
int main()
{
    int a,b;
    while(~scanf("%d%d", &a, &b))
    {
        printf("%d\n",a+b);
    }
    return 0;
}
```

# 1001: [编程入门] 第一个HelloWorld程序
```c
#include<stdio.h>
int main()
{
	printf("**************************\n");
	printf("Hello World!\n");
	printf("**************************\n");
	return 0;
}
```

# 1002: [编程入门] 三个数最大值
```c
#include<stdio.h>
int main()
{
	int a, b, c;
	scanf("%d%d%d", &a, &b, &c);
	int max;
	max = a;
	if (b > max)
	{
		max = b;
	}
	if(c > max)
	{
		max = c;
	}
	printf("%d", max);
	return 0;
}
```

# 1003: [编程入门] 密码破译
```c
#include<stdio.h>
int main()
{
    char china[5];
    scanf("%s", &china);
    for (int i = 0; i < 5; i++)
    {
        china[i] = china[i] + 4;
    }
	printf("%s\n", china);
	return 0;
}
```

# 1005: [编程入门] 温度转换
```c
#include<stdio.h>
int main()
{
	float ht, st;
	scanf("%f", &ht);
	st = 5 * (ht - 32) / 9;
	printf("c=%.2f", st);
	return 0;
}
```

# 1006: [编程入门] 三个数找最大值
```c
#include<stdio.h>
int main()
{
    int a, b, c;
    int max;
	scanf("%d%d%d", &a, &b, &c);
	max = a;
	if (b > max)
	{
	    max = b;
	}
	if (c > max)
	{
	    max = c;
	}
	printf("%d\n", max);
	return 0;
}
```
# 1007: [编程入门] 分段函数求值
```c
#include<stdio.h>
int main()
{
    int x, y;
    scanf("%d", &x);
    if (x < 1)
    {
        y = x;
    }
    else if (x>=1 && x < 10)
    {
        y = 2 * x - 1;
    }
    else
    {
        y = 3 * x - 11; 
    }
	printf("%d\n", y);
	return 0;
}
```

# 1008: [编程入门] 成绩评定
```c
#include<stdio.h>
int main()
{
    int score;
    scanf("%d", &score);
    if (score >= 90)
    {
        printf("A\n");
    }
    else if (score >= 80 && score <= 89)
    {
        printf("B\n");
    }
    else if (score >= 70 && score <= 79)
    {
        printf("C\n");
    }
    else if (score >= 60 && score <= 69)
    {
        printf("D\n");
    }
    else
    {
        printf("E\n");
    }
	return 0;
}
```

# 1009: [编程入门] 数字的处理与判断
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[10];
	gets(str);
	printf("%d\n", strlen(str));
	for (int i = 0; i < strlen(str) - 1; i++)
	{
	    printf("%c ", str[i]);
	}
	printf("%c\n", str[strlen(str) - 1]);
	for (int i = strlen(str) - 1; i > 0; i--)
	{
	    printf("%c", str[i]);
	}
	printf("%c\n", str[0]);
	return 0;
}
```
# 1010: [编程入门] 利润计算
```c
#include<stdio.h>
int main()
{
    int lirun, jiangjin;
    scanf("%d", &lirun);
    if (lirun <= 100000)
    {
        jiangjin = lirun * 0.1;
    }
    else if (lirun > 100000 && lirun <= 200000)
    {
        jiangjin = 100000 * 0.1;
        jiangjin = jiangjin + (lirun - 100000) * 0.075;
    }
    else if (lirun > 200000 && lirun <= 400000)
    {
        jiangjin = 100000 * 0.1;
        jiangjin = jiangjin + 100000 * 0.075;
        jiangjin = jiangjin + (lirun - 200000) * 0.05;        
    }
    else if (lirun > 400000 && lirun <= 600000)
    {
        jiangjin = 100000 * 0.1;
        jiangjin = jiangjin + 100000 * 0.075;
        jiangjin = jiangjin + 200000 * 0.05;
        jiangjin = jiangjin + (lirun - 400000) * 0.03;
    }
    else if (lirun >600000 && lirun <= 1000000)
    {
        jiangjin = 100000 * 0.1;
        jiangjin = jiangjin + 100000 * 0.075;
        jiangjin = jiangjin + 200000 * 0.05;
        jiangjin = jiangjin + 200000 * 0.03;
        jiangjin = jiangjin + (lirun - 600000) * 0.015;
    }
    else if (lirun > 1000000)
    {
        jiangjin = 100000 * 0.1;
        jiangjin = jiangjin + 100000 * 0.075;
        jiangjin = jiangjin + 200000 * 0.05;
        jiangjin = jiangjin + 200000 * 0.03;
        jiangjin = jiangjin + 400000 * 0.015;
        jiangjin = jiangjin + (lirun - 1000000) * 0.01;
    }    
	printf("%d\n", jiangjin);
	return 0;
}
```

# 1012: [编程入门] 字符串分类统计
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[200];
	gets(str);
	int z = 0, s = 0, k = 0, q = 0;
	for (int i = 0; i < strlen(str); i++)
	{
	    //大写字母
	    if (str[i] >= 65 && str[i] <= 90)
	    {
	        z++;
	    }
	    else if (str[i] >= 97 && str[i] <= 122)    //小写字母
	    {
	        z++;
	    }
	    else if (str[i] >= 48 && str[i] <= 57)    //数字
	    {
	        s++;
	    }
	    else if (str[i] == 32)    //空格
	    {
	        k++;
	    }
	    else    //其它字符
	    {
	        q++;
	    }
	}
	printf("%d %d %d %d\n", z, s, k, q);
	return 0;
}
```

# 1013: [编程入门] Sn的公式求和
```c
#include<stdio.h>
#include<math.h>
int main()
{
    int n;
    scanf("%d", &n);
    int sum, all = 0;
    for (int i = 0; i < n; i++)
    {
        sum = 0;
        for (int j = 0; j < i + 1; j++)
        {
            sum = sum + 2 * pow(10, j);
        }
        all = all + sum;
    }
	printf("%d\n", all);
	return 0;
}
```

# 1015: [编程入门] 求和训练
```c
#include<stdio.h>
#include<math.h>
int main()
{
	int a, b, c;
	float sum, sum1=0, sum2=0, sum3=0;
	scanf("%d%d%d", &a, &b, &c);
	for (int i = 1; i <= a; i++)
	{
		sum1 = sum1 + i;
	}
	for (int i = 0; i <= b; i++)
	{
		sum2 = sum2 + pow(i, 2);
	}
	for(int i = 1; i <= c; i++)
	{
		sum3 = sum3 + pow(i, -1);
	}
	sum = sum1 + sum2 + sum3;
	printf("%.2f\n", sum);
	return 0;
}
```

# 1018: [编程入门] 有规律的数列求和
```c
#include<stdio.h>
int main()
{
    int n;
    scanf("%d", &n);
    float fenzi[n], fenmu[n];
    float sum = 0;
    for (int i = 0; i < n; i++)
    {
        if (i == 0)
        {
            fenzi[i] = 2;
            fenmu[i] = 1;
        }
        else if (i == 1)
        {
            fenzi[i] = 3;
            fenmu[i] = 2;            
        }
        else
        {
            fenzi[i] = fenzi[i - 2] + fenzi[i - 1];
            fenmu[i] = fenmu[i - 2] + fenmu[i - 1];
        }
    }
    
    for (int i = 0; i < n; i ++)
    {
        sum = sum + (fenzi[i] / fenmu[i]);
    }
    printf("%.2f", sum);
	return 0;
}
```

# 1019: [编程入门] 自由下落的距离计算
```c
#include<stdio.h>
int main()
{
    float m, height, path;
    int n;
    scanf("%f%d", &m, &n);
    height = m;
    path = 0;
    //前n-1次 
    for (int i = 0; i < (n - 1); i++)
    {
        path = path + height;
        path = path + 0.5 * height;
        height = 0.5 * height;
    }
    //第n次
    path = path + height;
    height = 0.5 * height;
	printf("%.2f %.2f\n", height, path);
	return 0;
}
```

# 1020: [编程入门] 猴子吃桃的问题
```c
#include<stdio.h>
int main()
{
	//天数
	int n;
	scanf("%d", &n);
	
	//桃子总数
	int zongshu;
	
	for (int i = n; i > 0; i--)
	{
		if (i == n)
		{
			zongshu = 1;
		}
		else
		{
			zongshu = (zongshu + 1) * 2;
		}
	}
	printf("%d\n", zongshu);
	return 0;
}
```

# 1022: [编程入门] 筛选N以内的素数
```c
#include<stdio.h>
int main()
{
    int n, prime;
    scanf("%d", &n);
    for (int i = 2; i <= n; i++)
    {
        prime = 1;
        for (int j = 1; j < i; j++)
        {
            if (i % j == 0 && j != 1 && j != i)
            {
                prime = 0;
                break;
            }
        }
        if (prime == 1)
        {
            printf("%d\n", i);
        }
    }
	return 0;
}
```

# 1024: [编程入门] 矩阵对角线求和
```c
#include<stdio.h>
#include<math.h>
int main()
{
	int juzhen[3][3];
	for(int i=0; i < 3; i++)
	{
		for(int j=0; j < 3; j++)
		{
			scanf("%d", &juzhen[i][j]);
		}
		
	}
	int zhu = 0, fu = 0;
	for(int i=0; i < 3; i++)
	{
		for(int j=0; j < 3; j++)
		{
			if (i == j)
			{
				zhu = zhu + juzhen[i][j];
			}
			if ((i + j) == 2)
			{
				fu = fu + juzhen[i][j];
			}
		}
	}
	printf("%d %d", zhu, fu);	
	return 0;
}
```

# 1025: [编程入门] 数组插入处理
```c
#include<stdio.h>
#include<math.h>
int main()
{
	int s[9];
	for(int i=0; i < 9; i++)
	{
		scanf("%d", &s[i]);
	}
	int charu_value;
	int flag = 0;
	scanf("%d", &charu_value);
	for(int i=0; i < 9; i++)
	{
		if (flag == 0 && charu_value < s[i])
		{
			printf("%d\n", charu_value);
			flag = 1;
		}
		printf("%d\n", s[i]);
	}
	return 0;
}
```

# 1026: [编程入门] 数字逆序输出
```c
#include<stdio.h>
int main()
{
    int shuzi[10];
    for (int i = 0; i < 10; i++)
    {
        scanf("%d", &shuzi[i]);
    }
    for (int i = 9; i >= 0; i--)
    {
        if (i == 0)
        {
            printf("%d\n", shuzi[i]);    
        }
        else
        {
            printf("%d ", shuzi[i]);
        }
    }
	return 0;
}
```

# 1030: [编程入门] 二维数组的转置
```c
#include<stdio.h>
int main()
{
    int juzhen[3][3];
    //输入二维矩阵   
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            scanf("%d", &juzhen[i][j]);
        }
    }
    
    //生成二维矩阵的转置
    int zhuanzhi[3][3];
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            zhuanzhi[i][j] = juzhen[j][i];
        }
    }
    
    //输出转置后的二维矩阵
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            if (j == 2)
            {
                printf("%d\n", zhuanzhi[i][j]);
            }
            else
            {
                printf("%d ", zhuanzhi[i][j]);
            }
        }
    }
	return 0;
}
```

# 1131: C语言训练-斐波纳契数列
```c
#include<stdio.h>
int main()
{
    int n;
    int fbnq[40];
    scanf("%d", &n);
    fbnq[0] = 1;
    fbnq[1] = 1;
    for (int i = 2; i < n; i++)
    {
        fbnq[i] = fbnq[i - 2] + fbnq[i - 1];
    }
    for (int i = 0; i < n; i++)
    {
        if (i == (n -1)){
            printf("%d\n", fbnq[i]);
        }
        else
        {
            printf("%d ", fbnq[i]);
        }
    }
	return 0;
}
```

# 1032: [编程入门] 自定义函数之字符串连接
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char s1[100], s2[100];
	gets(s1);
	gets(s2);
	strcat(s1, s2);
	
	for(int i = 0; i < strlen(s1); i++)
	{
		if (i == (strlen(s1) - 1))
		{
			printf("%c\n", s1[i]);
		}
		else
		{
			printf("%c", s1[i]);
		}		
	}
	return 0;	
}
```

# 1033: [编程入门] 自定义函数之字符提取
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char s1[100], s2[100];
	gets(s1);
	int count = 0;
	int n = strlen(s1);
	for(int i = 0; i < n; i++)
	{
		if (s1[i] == 'a' | s1[i] == 'e' | s1[i] == 'i' | s1[i] == 'o' | s1[i] == 'u')
		{
			s2[count] = s1[i];
			count = count + 1;
		}
	}
	for(int i = 0; i < count; i++)
	{
		if (i == (count - 1))
		{
			printf("%c\n", s2[i]);
		}
		else
		{
			printf("%c", s2[i]);
		}
	}
	return 0;	
}
```

# 1035: [编程入门] 自定义函数之字符类型统计
```c
#include<stdio.h>
#include<string.h>
void string_kind(char str[])
{
	int z = 0, s = 0, k = 0, q = 0;
	for (int i = 0; i < strlen(str); i++)
	{
	    //大写字母
	    if (str[i] >= 65 && str[i] <= 90)
	    {
	        z++;
	    }
	    else if (str[i] >= 97 && str[i] <= 122)    //小写字母
	    {
	        z++;
	    }
	    else if (str[i] >= 48 && str[i] <= 57)    //数字
	    {
	        s++;
	    }
	    else if (str[i] == 32)    //空格
	    {
	        k++;
	    }
	    else    //其它字符
	    {
	        q++;
	    }
	}
	printf("%d %d %d %d\n", z, s, k, q);    
}
int main()
{
    char str[200];
    gets(str);
    string_kind(str);
	return 0;
}
```

# 1044: [编程入门] 三个字符串的排序
```c
#include<stdio.h>
#include<string.h>

int main()
{
	char str1[100], str2[100], str3[100], temp[100];
	gets(str1);
	gets(str2);
	gets(str3);
	//如果str1大于str2
	if(strcmp(str1, str2) > 0)
	{
		strcpy(temp, str1);
		strcpy(str1, str2);
		strcpy(str2, temp);
	}
	//如果str1大于str3
	if(strcmp(str1, str3) > 0)
	{
		strcpy(temp, str1);
		strcpy(str1, str3);
		strcpy(str3, temp);
	}	
	//如果str2大于str3
	if(strcmp(str2, str3) > 0)
	{
		strcpy(temp, str2);
		strcpy(str2, str3);
		strcpy(str3, temp);
	}	
	puts(str1);
	puts(str2);
	puts(str3);
	return 0;
}
```

# 1046: [编程入门] 自定义函数之数字后移
```c
#include<stdio.h>
#include<math.h>

int main ()
{
	//输入数据的个数
	int n;
	scanf("%d", &n);
	
	//定义两个长度为n的数组，其中num1为原始数组，num2为存储后的数组
	int num1[n], num2[n];
	
	//输入原始数组num1
	for (int i = 0; i < n; i++)
	{
		scanf("%d", &num1[i]);
	}
	
	//输入要移动的数字个数m
	int m;
	scanf("%d", &m);
	
	//将最后m个数移动到前面
	for(int i = 0; i < n; i++)
	{
		if (i < m)
		{
			num2[i] = num1[i + (n - m)];			
		}
		else
		{
			num2[i] = num1[i - m];	
		}
	}
	
	for (int i = 0; i < n; i++)
	{
		if (i < (n - 1))
		{
			printf("%d ", num2[i]);
		}
		else
		{
			printf("%d\n", num2[i]);
		}
	}
	return 0;
}
```

# 1052: [编程入门] 链表合并
```c
#include<stdio.h>
#include<malloc.h>

//定义结构体和结构体指针
typedef struct _node
{
	int no;
	int score;
	struct _node *next;
}Node, *node;
//这样可以用Node定义结构体，node表示结构体指针


//创建链表
node createLink(int n);

//打印链表
void printLink(node p);

//合并两个链表
node mergeLink(node p1, node p2);

//排序链表
node sortLink(node p);

//主函数
int main()
{
	int n, m;
	scanf("%d%d", &n, &m);
	node head1 = createLink(n);
	node head2 = createLink(m);
	node head = mergeLink(head1, head2);
	sortLink(head);
	printLink(head);
	return 0;
}

node createLink(int n)
{
	node head = NULL; //定义要创建链表的头指针
	head = (node)malloc(sizeof(Node));
	head->next = NULL;
	node p = head;
	for(int i = 0; i < n; i++)
	{
		scanf("%d%d", &p->no, &p->score);
		if(i == (n - 1))
		{
			p->next = NULL;
		}
		else
		{
			p->next = (node)malloc(sizeof(Node));
		}
		p = p->next;	
	}
	return head;
}

void printLink(node p)
{
	while(p)
	{
		printf("%d %d\n", p->no, p->score);
		p = p->next;
	}
}

node mergeLink(node p1, node p2)
{
	node head = p1;
	//先将p1移动到最后一个节点
	while(p1->next != NULL)
	{
		p1 = p1->next;
	}
	p1->next = p2;
	return head;
}

node sortLink(node p)
{
	node head = p;
	while(p != NULL)
	{
		node q = p;
		int minno = p->no;
		node minp = NULL;
		while(q != NULL)
		{
			if(q->no < minno)
			{
				minno = q->no;
				minp = q;
			}
			q = q->next;
		}
		
		if(minp != NULL)
		{
			int tmpno, tmpscore;
			tmpno = p->no;
			tmpscore = p->score;
			p->no = minp->no;
			p->score = minp->score;
			minp->no = tmpno;
			minp->score = tmpscore;
		}
		
		p = p->next;
	}
	return head;
}
```


# 1053: 二级C语言-平均值计算
```c
#include<stdio.h>
int main()
{
	int num[10];
	for (int i = 0; i < 10; i++)
	{
		scanf("%d", &num[i]);
	}	
	float avg = 0;
	for(int i = 0; i < 10; i++)
	{
		avg = avg + num[i]; 
	}
	avg = avg / 10;	
	int count = 0;
	for(int i = 0; i < 10; i++)
	{
		if (num[i] > avg)
		{
			count = count + 1;
		}
	}	
	printf("%d\n", count);
	return 0;	
}
```

# 1061: 二级C语言-计负均正
```c
#include<stdio.h>
int main()
{
	int num[20];
	for (int i = 0; i < 20; i++)
	{
		scanf("%d", &num[i]);
	}
	int fc = 0, zc = 0;
	float zavg = 0;
	for(int i = 0; i < 20; i++)
	{
		if (num[i] > 0)
		{
			zc = zc + 1;
			zavg = zavg + num[i];
		}
		else
		{
			fc = fc + 1;
		}
	}
	zavg = zavg / zc;
	printf("%d\n", fc);
	printf("%.2f\n", zavg);
	return 0;	
}
```

# 1065: 二级C语言-最小绝对值
```c
#include<stdio.h>
#include<math.h>
int main()
{
	int num[10];
	for(int i = 0; i < 10; i++)
	{
		scanf("%d", &num[i]);
	}
	int index = 0;
	for(int i = 1; i < 10; i++)
	{
		if(abs(num[i]) < abs(num[index]))
		{
			index = i;
		}
	}
	int ex;
	ex = num[index];
	num[index] = num[9];
	num[9] = ex;
	for (int i = 0; i < 10; i++)
	{
		if (i < 9)
		{
			printf("%d ", num[i]);
		}
		else
		{
			printf("%d\n", num[i]);
		}
	}
	return 0;	
}
```

# 1067: 二级C语言-分段函数
```c
#include<stdio.h>
#include<math.h>
int main()
{
    float x, fx;
    scanf("%f", &x);
    if (x < 0)
	{
		fx = fabs(x);
	}
	if (x >= 0 && x < 2)
	{
		fx = pow((x + 1), 0.5);
	}
	if (x >= 2 && x < 4)
	{
		fx = pow((x + 2), 5);
	}
	if (x >= 4)
	{
		fx = 2 * x + 5;
	}
	printf("%.2f", fx);
	return 0;
}
```

# 1069: 二级C语言-寻找矩阵最值
```c
#include<stdio.h>
#include<math.h>
int main()
{
	int n;
	scanf("%d", &n);
	int m[n][n];
	for(int i = 0; i < n; i++)
	{
		for(int j = 0; j < n; j++)
		{
			scanf("%d", &m[i][j]); 
		}
	}
	int indexi = 0, indexj = 0;
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			if (i == 0 && j == 0)
			{
				continue;
			}
			else
			{
				if (abs(m[i][j]) > abs(m[indexi][indexj]))
				{
					indexi = i;
					indexj = j;
				}
			}
		}
	}
	printf("%d %d %d\n", m[indexi][indexj], (indexi + 1), (indexj + 1));
	return 0;	
}
```

# 1085: A+B for Input-Output Practice (I)
```c
#include<stdio.h>
int main()
{
	int a, b;
	while(scanf("%d%d", &a, &b) != EOF)
	{
		printf("%d\n", a + b);
	}
	return 0;
}
```

# 1094: 字符串的输入输出处理
```c
#include<stdio.h>
#include<string.h>
int main()
{
	int n;
	scanf("%d", &n);
	getchar();
	for(int i = 0; i < n; i++)
	{
		char str1[1000];
		gets(str1);
		puts(str1);
		printf("\n");
	}
	char str2[1000];
	while((scanf("%s", &str2)) != EOF)
	{
		printf("%s\n\n", str2);
	}
	return 0;
}
```

# 1113: C语言考试练习题_保留字母
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char s1[200], s2[200];
	gets(s1);
	int index = 0;
	for(int i = 0; i < strlen(s1); i++)
	{
		if((s1[i] >= 65 && s1[i] <= 90) | (s1[i] >= 97 && s1[i] <= 122))
		{
			s2[index] = s1[i];
			index ++;
		}
	}	
	for(int i = 0; i < index; i++)
	{
		if(i == index - 1)
		{
			printf("%c\n", s2[i]);
		}
		else
		{
			printf("%c", s2[i]);	
		}
	}
	return 0;
}
```

# 1126: C语言训练-字符串正反连接
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char s1[50];
	gets(s1);
	int length = strlen(s1);
	for(int i = 0; i < length; i++)
	{
		printf("%c", s1[i]);
	}
	for(int i = (length - 1); i >= 0; i--)
	{
		if(i == 0)
		{
			printf("%c\n", s1[i]);
		}
		else
		{
			printf("%c", s1[i]);
		}
	}
	return 0;
}
```

# 1131: C语言训练-斐波纳契数列
```c
#include<stdio.h>
int main()
{
    int n;
    int fbnq[40];
    scanf("%d", &n);
    fbnq[0] = 1;
    fbnq[1] = 1;
    for (int i = 2; i < n; i++)
    {
        fbnq[i] = fbnq[i - 2] + fbnq[i - 1];
    }
    for (int i = 0; i < n; i++)
    {
        if (i == (n -1)){
            printf("%d\n", fbnq[i]);
        }
        else
        {
            printf("%d ", fbnq[i]);
        }
    }
	return 0;
}
```

# 1132: C语言训练-最大数问题
```c
#include<stdio.h>
int main ()
{
	int n, max;
	scanf("%d", &n);
	max = n;
	while(n != -1)
	{
		if (n > max)
		{
			max = n;
		}
		scanf("%d", &n);
	}
	printf("%d\n", max);
}
```

# 1135: C语言训练-求s=a+aa+aaa+aaaa+aa...a的值
```c
#include<stdio.h>
#include<math.h>
int main ()
{
	int a, n, s, sum;
	scanf("%d%d", &a, &n);
	s = 0;
	sum = 0;
	for(int i = 0; i < n ; i++)
	{
		s = s + a * pow(10, i);
		sum = sum + s;
	}
	printf("%d\n", sum);
	return 0;
}
```

# 1149: C语言训练-计算1~N之间所有奇数之和
```c
#include<stdio.h>
#include<math.h>
int main ()
{
	int n, sum;
	scanf("%d", &n);
	sum = 0;
	for(int i = 1; i <= n ; i++)
	{
		if (i % 2 == 1)
		{
			sum = sum + i;
		}
	}
	printf("%d\n", sum);
	return 0;
}
```

# 1150: C语言训练-计算t=1+1/2+1/3+...+1/n
```c
#include<stdio.h>
#include<math.h>
int main ()
{
	int n;
	double t = 0;
	scanf("%d", &n);
	for(int i = 1; i <= n ; i++)
	{
		t = t + pow(i, -1);
	}
	printf("%.6lf", t);
	return 0;
}
```

# 1205: 字符串的修改
```c
#include<stdio.h>
#include<string.h>
#include<math.h>

int main()
{
	char stra[201], strb[201];
	gets(stra);
	gets(strb);
	int lena, lenb, step;
	lena = strlen(stra);
	lenb = strlen(strb);
	step = 0;
	for(int i = 0; i < lena; i++)
	{
		for(int j = 0; j < lenb; j++)
		{
			if(stra[i] == strb[j])
			{
				step++;
				break;
			}
		}
	}
	step = lena - step;
	printf("%d\n", step);
	return 0;
}
```

# 1206: 字符串问题
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char str[256];
	gets(str);
	int len = strlen(str);
	for(int i = (len - 1); i >= 0; i--)
	{
		printf("%c", str[i]);
		if(i == 0)
		{
			printf("\n");
		}
	}
	return 0;
}
```

# 1207: 字符排列问题

```c
#include<stdio.h>
#include<string.h>
int main()
{
	int n;
	scanf("%d", &n);
	getchar();
	char str[n+1];
	gets(str);
	int len = strlen(str);
	
	int p; 
	p = 1;
	for(int i = 2; i < len + 1; i++)
	{
		p = p * i;
	}
	
	int count[52];
	for(int i = 0; i < 52; i++)
	{
		count[i] = 0;
	}
	
	for(int i = 0; i < len; i++)
	{
		int index;
		if(str[i] >= 'a' && str[i] <= 'z')
		{
			index = str[i] - 97;
		}
		else if(str[i] >= 'A' && str[i] <= 'Z') 
		{
			index = str[i] - 39;
		}
		count[index]++;
	}
	
	for(int i = 0; i < 52; i++)
	{
		if(count[i] > 1)
		{
			int jiecheng = 1;
			for(int j = 2; j <= count[i]; j++)
			{
				jiecheng = jiecheng * j;
			}
			p = p / jiecheng;
		}
	}
	printf("%d\n", p);
	return 0;
}
```

# 1209: 密码截获

```c
#include<stdio.h>
#include<string.h>
int main()
{
	//先开一个数组
	char str[200];
	
	//多组输入输出数据用while
	while(gets(str))
	{
		//最长回文子串的长度
		int max_length;
	
		//将max_length的长度先赋值为1
		max_length = 1;
		
		int length;
		length = strlen(str);
		for(int i = 0; i < length; i++)
		{
			for(int j = i; j < length; j++)
			{
				int flag; //定义一个标志位
				flag = 1; //flag = 1时，表示字符串是回文
				int p, q;
				for(p = i, q = j; p < q; p++, q--)
				{
					if(str[p] != str[q])
					{
						flag = 0;
						break;
					}
				}
				//如果是回文
				if(flag == 1)
				{
					int hlen;
					hlen = j - i + 1;
					if(hlen > max_length)
					{
						max_length = hlen;
					}
				}
			}
		}
		printf("%d\n", max_length);
	}
	return 0;
}
```
# 1429: 蓝桥杯2014年第五届真题-兰顿蚂蚁

```c
#include<stdio.h>
//定义蚂蚁结构体
struct ant
{
	int x; //x坐标
	int y; //y坐标
	char c; //朝向
};

int main()
{
	int m, n;
	scanf("%d%d", &m, &n);
	int map[m][n];
	for(int i = 0; i < m; i++)
	{
		for(int j = 0; j < n; j++)
		{
			scanf("%d", &map[i][j]);
		}
	}
	
	int x, y, k;
	char c;
	scanf("%d %d %c %d", &x, &y, &c, &k);
		
	//开一个mayi的结构体	
	struct ant mayi;
	mayi.x = x;
	mayi.y = y;
	mayi.c = c;
	
	while(k)
	{
		if(map[mayi.x][mayi.y] == 1)  //如果蚂蚁在黑格
		{
			//将该格变为白格
			map[mayi.x][mayi.y] = 0;
			
			//右转90度
			if(mayi.c == 'U')
			{
				mayi.c = 'R';
				mayi.y++;	
			}
			else if(mayi.c == 'D')
			{
				mayi.c = 'L';
				mayi.y--;
			}
			else if(mayi.c == 'L')
			{
				mayi.c = 'U';
				mayi.x--;
			}
			else if(mayi.c == 'R')
			{
				mayi.c = 'D';
				mayi.x++;
			}			
		}	
		else if(map[mayi.x][mayi.y] == 0)  //如果蚂蚁在白格
		{
			//将该格变为黑格
			map[mayi.x][mayi.y] = 1;
			
			//左转90度
			if(mayi.c == 'U')
			{
				mayi.c = 'L';
				mayi.y--;	
			}
			else if(mayi.c == 'D')
			{
				mayi.c = 'R';
				mayi.y++;
			}
			else if(mayi.c == 'L')
			{
				mayi.c = 'D';
				mayi.x++;
			}
			else if(mayi.c == 'R')
			{
				mayi.c = 'U';
				mayi.x--;
			}
		}	
		k--;
	}
	
	printf("%d %d", mayi.x, mayi.y);
	return 0;
}
```

# 1431: 蓝桥杯2014年第五届真题-分糖果

```c
#include<stdio.h>

int main()
{
	int n;
	scanf("%d", &n);
	int candy[n];
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &candy[i]);
	}
	
	
	int buchong = 0;
	while(1)
	{
		int flag = 1;
		for(int i = 0; i < n; i++)
		{
			if((candy[i] - candy[0]) != 0) //如果每个小孩的糖果数量存在不同
			{
				flag = 0;
				break;
			}
		}
		
		//如果每个小孩的糖果数量相同那么就停止了，跳出当前的while循环
		if(flag == 1)
		{
			break;
		}
		
		//计算每个孩子可以从右边的孩子那得到多少糖果
		int transfer[n];
		for(int i = 0; i < n; i++)
		{
			if(i == (n - 1))
			{
				transfer[i] = candy[0] / 2;
			}
			else
			{
				transfer[i] = candy[i + 1] / 2;
			}
		}
		
		//经过传递后每个孩子手中糖果数
		for(int i = 0; i < n; i++)
		{
			candy[i] = candy[i] / 2 + transfer[i]; 
		}
		
		//判断每个孩子手中糖果数，如果是奇数则老师给补1个
		for(int i = 0; i < n; i++)
		{
			if(candy[i] % 2 != 0)
			{
				candy[i]++;
				buchong++;
			}
		}
	}
	printf("%d\n", buchong);
	return 0;
}
```

# 1434: 蓝桥杯历届试题-回文数字

```c
#include<stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	int count;
	count = 0;
	for(int i = 10000; i < 1000000; i++)
	{
		int number, digit_sum, length;
		number = i;
		digit_sum = 0;
		length = 0;
		int shuzi[6];
		while(number)
		{
			shuzi[length] = number % 10;
			digit_sum = digit_sum + shuzi[length];
			number = number / 10;
			length++;
		}
		
		if(digit_sum == n)
		{
			int flag;
			//flag=1表示该数字是回文数字
			flag = 1;
			int p, q;
			for(p = 0, q = (length - 1); p < q; p++, q--)
			{
				if(shuzi[p] != shuzi[q])
				{
					flag = 0;
				}
			}
			
			//如果是回文数字则输出
			if(flag == 1)
			{
				printf("%d\n", i);
				count++;				
			}
		}
	}
	
	if(count == 0)
	{
		printf("-1\n");
	}	
	return 0;
}
```

# 1468: 蓝桥杯基础练习VIP-报时助手

```c
#include<stdio.h>
#include<string.h>

int main()
{
	//h保存小时数，m保存分钟数
	int h, m;
	
	//hshiwei保存小时数的十位，hgewei保存小时数的个位，mshiwei保存分钟数的十位，mgewei保存分钟数的个位
	int hshiwei, hgewei, mshiwei, mgewei;
	
	//输入小时数和分钟数
	scanf("%d%d", &h, &m);
	
	//将所有用到的跟时间相关的英文单词用一个二维char型数组保存
	char timeword[25][10] = {"zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine", "ten", "eleven", "twelve", "thirteen", "fourteen", "fifteen", "sixteen", "seventeen", "eighteen", "nineteen", "twenty", "thirty", "forty", "fifty", "o'clock"};
	
	//如果小时数小于20
	if(h < 20)
	{
		printf("%s", timeword[h]);
	}
	else //如果小时数在20-60之间
	{
		//求小时数的十位和个位数字
		hshiwei = h / 10;
		hgewei = h % 10;
		
		//输出小时数的十位数字
		printf("%s", timeword[18 + hshiwei]);
		
		//如果小时数的个位数字不为0，则输出
		if(hgewei != 0)
		{
			printf(" %s", timeword[hgewei]);
		}
	}
	
	//如果分钟数为0，上面处理完小时数后加o'clcok即可
	if(m == 0)
	{
		printf(" %s\n", timeword[24]);		
	}
	else //如果分钟数不为0，继续处理分钟数
	{
		//如果分钟数小于20
		if(m < 20)
		{
			printf(" %s\n", timeword[m]);
		}
		else
		{
			//求分钟数的十位和个位数字
			mshiwei = m / 10;
			mgewei = m % 10;
			
			//输出分钟数的十位数字
			printf(" %s", timeword[18 + mshiwei]);
		
			//如果分钟数的个位数字不为0，则输出
			if(mgewei != 0)
			{
				printf(" %s\n", timeword[mgewei]);
			}
			else
			{
				printf("\n");
			}			
		}
	}
	return 0;
}
```

# 1470: 蓝桥杯基础练习VIP-时间转换

```c
#include<stdio.h>
int main()
{
	int time, h, m, s;
	scanf("%d", &time);
	h = time / 3600;
	m = (time % 3600) / 60;
	s = (time % 3600) % 60;
	printf("%d:%d:%d\n", h, m, s);
	return 0;	
}
```

# 1476: 蓝桥杯基础练习VIP-龟兔赛跑预测

```c
#include<stdio.h>
int main()
{
	int v1, v2, t, s, l;
	scanf("%d%d%d%d%d", &v1, &v2, &t, &s, &l);
	
	//计时器
	int second = 0;
	
	//兔子跑动距离
	int distance_tuzi = 0;
	
	//乌龟跑动距离
	int distance_wugui = 0;
	
	//领先者跑动的距离
	int distance = 0;
	
	//兔子停留时间
	int stop_time = 0;
	
	//开始跑
	while(distance < l) //当领先的人跑动终点，即distance == l时跳出循环
	{
		//乌龟啥也不管就一直跑
		distance_wugui = distance_wugui + v2;
		
		//判断兔子现在是否在休息
		if(stop_time == 0) 
		{
			distance_tuzi = distance_tuzi + v1;
		}
		else //这一秒兔子不跑了，休息时间-1
		{
			stop_time--;
		}
		
		//如果兔子领先乌龟t米
		if((distance_tuzi - distance_wugui) >= t && stop_time == 0)
		{
			stop_time = s;
		}

		//计算领先者跑了多少米以判断是否到达重点
		if(distance_tuzi > distance_wugui)
		{
			distance = distance_tuzi;
		}
		else
		{
			distance = distance_wugui;
		}
		
		//计时器+1秒
		second++;
	}
	
	if(distance_wugui > distance_tuzi)
	{
		printf("T\n");
	}else if(distance_tuzi > distance_wugui)
	{
		printf("R\n");
	}else if(distance_tuzi == distance_wugui)
	{
		printf("D\n");
	}
	
	printf("%d\n", second);
			
	return 0;
}
```

# 1479: 蓝桥杯算法提高VIP-删除数组中的0元素

```c
#include<stdio.h>

int main()
{
	int num;
	scanf("%d", &num);
	int numbers1[num];
	for (int i = 0; i < num; i++)
	{
		scanf("%d", &numbers1[i]);
	}
	int count = 0;
	int numbers2[num];
	for(int i = 0; i < num; i++)
	{
		if(numbers1[i] != 0)
		{
			numbers2[count] = numbers1[i];
			count++;
		}
	}
	for(int i = 0; i < count; i++)
	{
		if(i == (count - 1))
		{
			printf("%d\n", numbers2[i]);
		}
		else
		{
			printf("%d ", numbers2[i]);	
		}
	}
	printf("%d", count);
	return 0;	
}
```

# 1486: 蓝桥杯算法提高VIP-一元一次方程

```c
#include<stdio.h>
int main()
{
	double a, b;
	double x;
	scanf("%lf%lf", &a, &b);
	x = -1.0 * b / a;
	printf("%.2lf\n", x);
	return 0;	
}
```

# 1508: 蓝桥杯算法提高VIP-和最大子序列

1. **暴力枚举**：不出意外的超时，算法的时间复杂度为$O(n^{3})$。

```c
#include<stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	int numbers[n];
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &numbers[i]);
	}
	
	//题中要求是连续子序列
	int max_value = numbers[0];
	for(int i = 0; i < n; i++)
	{
		for(int j = i; j < n; j++)
		{
			int sum = 0;
			for(int p = i; p <= j; p++)
			{
				sum = sum + numbers[p];
			}
			if(sum > max_value)
			{
				max_value = sum;
			}
		}
	}
	printf("%d\n", max_value);
	return 0;
}
```

2. **动态规划**：YYDS登场，算法时间复杂度为$O(n)$。

```c
#include<stdio.h>
int main()
{
	int n;
	scanf("%d", &n);
	int numbers[n];
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &numbers[i]);
	}
	
	int dp[n];
	dp[0] = numbers[0];
	for(int i = 1; i < n; i++)
	{
		if((dp[i - 1] + numbers[i]) > numbers[i])
		{
			dp[i] = dp[i - 1] + numbers[i];
		}
		else
		{
			dp[i] = numbers[i];
		}
	}
	
	int max_value = numbers[0];
	for(int i = 0; i < n; i++)
	{
		if(dp[i] > max_value)
		{
			max_value = dp[i];
		}
	}
	printf("%d\n", max_value);
	return 0;
}
```


# 1509: 蓝桥杯算法提高VIP-图形输出

```c
#include<stdio.h>
int main()
{
	printf(" X | X | X \n");
	printf("---+---+---\n");
	printf("   |   |   \n");
	printf("---+---+---\n");
	printf(" O | O | O \n");
	return 0;	
}
```


# 1512: 蓝桥杯算法提高VIP-多项式输出
```c
#include<stdio.h>
int main()
{
	//输入一元多项式的次数
	int n;
	scanf("%d", &n);
	
	//输入多项式的系数
	int xishu[n];
	for(int i = 0; i < (n + 1); i++)
	{
		scanf("%d", &xishu[i]);
	}
	
	for(int i = 0; i < n + 1; i++)
	{
		if(i == 0) //第一项的系数必不为0
		{
			if(xishu[i] > 0)
			{
				if(xishu[i] == 1)
				{
					printf("x^%d", (n - i));					
				}
				else
				{
					printf("%dx^%d", xishu[i], (n - i));					
				}
			}
			else
			{
				if(xishu[i] == -1)
				{
					printf("-x^%d", (n - i));					
				}
				else
				{
					printf("%dx^%d", xishu[i], (n - i));					
				}				
			}
		}	
		else if(i == n) //最后一项
		{
			if(xishu[i] == 0)
			{
				printf("\n");
			}
			else if(xishu[i] > 0)
			{
				printf("+%d\n", xishu[i]);
			}
			else
			{
				printf("%d\n", xishu[i]);
			}
		}
		else //中间项
		{
			if(xishu[i] == 0)
			{
				continue;
			}
			else if(xishu[i] > 0)
			{
				if(xishu[i] == 1)
				{
					if((n - i) == 1)
					{
						printf("+x");
					}
					else
					{
						printf("+x^%d", (n - i));						
					}
					
				}
				else
				{
					if((n - i) == 1)
					{
						printf("+%dx", xishu[i]);	
					}
					else
					{
						printf("+%dx^%d", xishu[i], (n - i));							
					}
				}				
			}
			else
			{
				if(xishu[i] == -1)
				{
					if((n - i) == 1)
					{
						printf("-x");
					}
					else
					{
						printf("-x^%d", (n - i));			
					}
				}
				else
				{
					if((n - i) == 1)
					{
						printf("%dx", xishu[i]);						
					}
					else
					{
						printf("%dx^%d", xishu[i], (n - i));						
					}	
				}				
			}
		}
	}
	return 0;
}
```

# 1520: 蓝桥杯算法提高VIP-开灯游戏
```c
#include<stdio.h>
#include<math.h>

int main()
{
	//定义数组保存灯的开或关状态，deng[i] = 0表示熄灭，反之表示点亮
	int deng[9];
	
	//最开始所有灯都是熄灭的
	for(int i = 0; i < 9; i++)
	{
		deng[i] = 0;
	}
	
	//求一共有多少中开关的组合方式
	int total = pow(2, 9);
	

	//初始化开关的开闭方式
	int kaiguan_bin[total][9];
	for(int i = 0; i < total; i++)
	{
		for(int j = 0; j < 9; j++)
		{
			kaiguan_bin[i][j] = 0;	
		}
	}
	
	//遍历每种方案	
	for(int i = 0; i < total; i++)
	{
		//将i转换成二进制表示形式
		int num = i;
		int index = 8;
		while(num)
		{
			kaiguan_bin[i][index] = num % 2;
			index--;
			num = num / 2;
		}
		
		if(kaiguan_bin[i][8] == 1)
		{
			//第二盏灯亮改变状态
			if(deng[1] == 0)
			{
				deng[1] = 1;
			}
			else
			{
				deng[1] = 0;
			}
			
			//第四盏灯亮改变状态
			if(deng[3] == 0)
			{
				deng[3] = 1;
			}
			else
			{
				deng[3] = 0;
			}				
		}
		
		if(kaiguan_bin[i][7] == 1)
		{
			//第一盏灯亮改变状态
			if(deng[0] == 0)
			{
				deng[0] = 1;
			}
			else
			{
				deng[0] = 0;
			}
			
			//第三盏灯亮改变状态
			if(deng[2] == 0)
			{
				deng[2] = 1;
			}
			else
			{
				deng[2] = 0;
			}
			
			//第五盏灯亮改变状态
			if(deng[4] == 0)
			{
				deng[4] = 1;
			}
			else
			{
				deng[4] = 0;
			}
		}
		
		if(kaiguan_bin[i][6] == 1)
		{
			//第二盏灯亮改变状态
			if(deng[1] == 0)
			{
				deng[1] = 1;
			}
			else
			{
				deng[1] = 0;
			}

			//第六盏灯亮改变状态
			if(deng[5] == 0)
			{
				deng[5] = 1;
			}
			else
			{
				deng[5] = 0;
			}
		}
		
		if(kaiguan_bin[i][5] == 1)
		{
			//第一盏灯亮改变状态
			if(deng[0] == 0)
			{
				deng[0] = 1;
			}
			else
			{
				deng[0] = 0;
			}
			
			//第五盏灯亮改变状态
			if(deng[4] == 0)
			{
				deng[4] = 1;
			}
			else
			{
				deng[4] = 0;
			}
			
			//第七盏灯亮改变状态
			if(deng[6] == 0)
			{
				deng[6] = 1;
			}
			else
			{
				deng[6] = 0;
			}
		}
		
		if(kaiguan_bin[i][4] == 1)
		{
			//第二盏灯亮改变状态
			if(deng[1] == 0)
			{
				deng[1] = 1;
			}
			else
			{
				deng[1] = 0;
			}
			
			//第四盏灯亮改变状态
			if(deng[3] == 0)
			{
				deng[3] = 1;
			}
			else
			{
				deng[3] = 0;
			}
			
			//第六盏灯亮改变状态
			if(deng[5] == 0)
			{
				deng[5] = 1;
			}
			else
			{
				deng[5] = 0;
			}

			//第八盏灯亮改变状态
			if(deng[7] == 0)
			{
				deng[7] = 1;
			}
			else
			{
				deng[7] = 0;
			}
		}
		
		if(kaiguan_bin[i][3] == 1)
		{
			//第三盏灯亮改变状态
			if(deng[2] == 0)
			{
				deng[2] = 1;
			}
			else
			{
				deng[2] = 0;
			}
			
			//第五盏灯亮改变状态
			if(deng[4] == 0)
			{
				deng[4] = 1;
			}
			else
			{
				deng[4] = 0;
			}

			//第九盏灯亮改变状态
			if(deng[8] == 0)
			{
				deng[8] = 1;
			}
			else
			{
				deng[8] = 0;
			}
		}
		
		if(kaiguan_bin[i][2] == 1)
		{
			//第四盏灯亮改变状态
			if(deng[3] == 0)
			{
				deng[3] = 1;
			}
			else
			{
				deng[3] = 0;
			}
			
			//第八盏灯亮改变状态
			if(deng[7] == 0)
			{
				deng[7] = 1;
			}
			else
			{
				deng[7] = 0;
			}
		}
		
		if(kaiguan_bin[i][1] == 1)
		{
			//第五盏灯亮改变状态
			if(deng[4] == 0)
			{
				deng[4] = 1;
			}
			else
			{
				deng[4] = 0;
			}
			
			//第七盏灯亮改变状态
			if(deng[6] == 0)
			{
				deng[6] = 1;
			}
			else
			{
				deng[6] = 0;
			}

			//第九盏灯亮改变状态
			if(deng[8] == 0)
			{
				deng[8] = 1;
			}
			else
			{
				deng[8] = 0;
			}
		}
		
		if(kaiguan_bin[i][0] == 1)
		{
			//第六盏灯亮改变状态
			if(deng[5] == 0)
			{
				deng[5] = 1;
			}
			else
			{
				deng[5] = 0;
			}
			
			//第八盏灯亮改变状态
			if(deng[7] == 0)
			{
				deng[7] = 1;
			}
			else
			{
				deng[7] = 0;
			}
		}
		
		int count = 0;
		//查一查有几盏灯是亮的
		for(int j = 0; j < 9; j++)
		{
			if(deng[j] == 1)
			{
				count++;
			}
		}
		
		if(count == 4)
		{
			for(int j = 0; j < 9; j++)
			{
				if(j == 8)
				{
					printf("%d\n", kaiguan_bin[i][j]);
				}
				else
				{
					printf("%d", kaiguan_bin[i][j]);					
				}
			}
		}
		
		for(int j = 0; j < 9; j++)
		{
			deng[j] = 0;
		}
	}
	return 0;
}
```


# 1543: 蓝桥杯算法提高VIP-淘淘的名单
```c
#include<stdio.h>
#include<string.h>

int main()
{
	int n;
	scanf("%d", &n);
	while(n)
	{
		char name[6];
		scanf("%s", &name);
		if(strcmp(name, "WYS") == 0)
		{
			printf("KXZSMR\n");
		}
		else if(strcmp(name, "CQ") == 0)
		{
			printf("CHAIQIANG\n");
		}
		else if(strcmp(name, "LC") == 0)
		{
			printf("DRAGONNET\n");
		}
		else if(strcmp(name, "SYT") == 0 || strcmp(name, "SSD") == 0 || strcmp(name, "LSS") == 0 || strcmp(name, "LYF") == 0)
		{
			printf("STUDYFATHER\n");
		}
		else
		{
			printf("DENOMINATOR\n");
		}		
		n--;
	}
	return 0;
}
```

# 1557: 蓝桥杯算法提高VIP-聪明的美食家

**1. 递归解法**：也称暴力枚举，算法的时间复杂度会爆炸，仅供参考，在OJ上提交会提示超时。
```c
#include<stdio.h>

//小吃街上小吃的数量
int n;

//n种食物的美味度
int meiweidu[1000];

//函数length返回数组meiweidu从i开始的最长子序列长度
int length(int i)
{
	//当i是meweidu这个数组中最后一个值时，后面没有值了，也无法构成子序列了
	if(i == (n - 1))
	{
		return 1;
	}
	
	int max_length = 1;
	for(int j = (i + 1); j < n; j++)
	{
		//可以构成递增序列
		if(meiweidu[j] >= meiweidu[i])
		{
			int l = length(j) + 1;
			if(l > max_length)
			{
				max_length = l;
			}
		}
	}
	return max_length;
}

//返回最长递增子序列的长度
int zcdzzxl()
{
	int max_length = 1;
	for(int i = 0; i < n; i++)
	{
		int l = length(i);
		if(l > max_length)
		{
			max_length = l;
		}
	}
	return max_length;
}

int main()
{
	scanf("%d", &n);	
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &meiweidu[i]);
	}
	int max_length;
	max_length = zcdzzxl();
	printf("%d\n", max_length);
	return 0;
}
```

**2. 动态规划解法**：Dynamic Programming，YYDS。

```c
#include<stdio.h>
int main()
{
	//小吃街上小吃的数量
	int n;
	scanf("%d", &n);
		
	//n种食物的美味度
	int meiweidu[n];
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &meiweidu[i]);
	}
	
	/*动态规划求解*/
	//定义dp数组，dp[i]表示以i为终点的最长递增子序列的长度
	int dp[n];
	
	//初始化dp数组，将所有值都置为1
	for(int i = 0; i < n; i++)
	{
		dp[i] = 1;	
	}
	
	//从索引为1开始遍历
	for(int i = 1; i < n; i++)
	{
		for(int j = 0; j < i; j++)
		{
			if(meiweidu[j] <= meiweidu[i])
			{
				if((dp[j] + 1) > dp[i])
				{
					dp[i] = dp[j] + 1;
				}
			}
		}
	}	
	
	int max_length = 1;
	for(int i = 0; i < n; i++)
	{
		if(dp[i] > max_length)
		{
			max_length = dp[i];
		}
	}
	
	printf("%d\n", max_length);
	return 0;
}
```

# 1579: 蓝桥杯算法提高VIP-陶陶摘苹果2

```c
#include<stdio.h>
int main()
{
	int n, m;
	scanf("%d%d", &n, &m);
	int height[n];
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &height[i]);
	}
	int count = 0;
	for(int i = 0; i < n; i++)
	{
		if((m + 30) < height[i])
		{
			count++;
		}
	}
	printf("%d", count);
	return 0;	
}
```

# 1585: 蓝桥杯算法训练VIP-链表数据求和操作
```c
#include<stdio.h>
#include<malloc.h>

//定义结构体和结构体指针
typedef struct _node
{
	int shi;
	int xu;
	struct _node *next;
}Node, *node;

int main()
{
	node head = (node)malloc(sizeof(Node));
	node p = head;
	for(int i = 0; i < 10; i++)
	{
		scanf("%d%d", &p->shi, &p->xu);
		if(i == 9){
			p->next = NULL;
		}
		else
		{
			p->next = (node)malloc(sizeof(Node));
		}
		p = p->next;
	}
	
	int shi = 0, xu = 0;
	while(head != NULL)
	{
		shi = shi + head->shi;
		xu = xu + head->xu;
		head = head->next;
	}
	
	if(xu > 0)
	{
		printf("%d+%di", shi, xu);
	}
	else
	{
		printf("%d%d", shi, xu);		
	}
	return 0;
}
```

# 1627: 蓝桥杯算法训练VIP-拦截导弹

```c
#include<stdio.h>
#include<string.h>

int main()
{
	//输入来袭导弹的高度
	int height[10000];
	int index = 0;
	char c = ' ';
	while(c == ' ')
	{
		scanf("%d", &height[index]);
		index++;
		c = getchar();
	}
	
	//求最长递减子序列
	//定义dp数组，dp[i]表示的是以i为结尾的最长递减子序列长度
	int dp[index];
	dp[0] = 1;
	for(int i = 1; i < index; i++)
	{
		int max_length = 1;
		for(int j = 0; j < i; j++)
		{
			if(height[j] >= height[i])
			{
				if((dp[j] + 1) > max_length)
				{
					max_length = dp[j] + 1;
				}
			}			
		}
		dp[i] = max_length;
	}
	
	//求最大能拦截多少个导弹
	int max_lanjie = 0;
	for(int i = 0; i < index; i++)
	{
		if(dp[i] > max_lanjie)
		{
			max_lanjie = dp[i];
		}
	}
	
	//求最长递增子序列长度
	int dp2[index];
	dp2[0] = 1;
	for(int i = 1; i < index; i++)
	{
		int max_length2 = 1;
		for(int j = 0; j < i; j++)
		{
			if(height[j] <= height[i])
			{
				if((dp2[j] + 1) > max_length2)
				{
					max_length2 = dp2[j] + 1;
				}
			}
		}
		dp2[i] = max_length2;
	}
	
	//求最少需要多少个拦截系统
	int min_xitong = 1;
	for(int i = 0; i < index; i++)
	{
		if(dp2[i] > min_xitong)
		{
			min_xitong = dp2[i];
		}
	}
	printf("%d\n", max_lanjie);
	printf("%d\n", min_xitong);
	return 0;
}
```

# 1633: 蓝桥杯算法训练VIP-数的统计
```c
#include<stdio.h>

int tongji[1000000];

int main()
{
	int n;
	scanf("%d", &n);
	
	int numbers[n];
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &numbers[i]);
	}
	
	for(int i = 0; i < n; i++)
	{
		tongji[numbers[i]]++;
	}
	
	for(int i = 0; i < 1000000; i++)
	{
		if(tongji[i] != 0)
		{
			printf("%d %d\n", i, tongji[i]);
		}
	}
	return 0;
}
```


# 1668: printf基础练习2

```c
#include<stdio.h>
int main()
{
	int a;
	scanf("%d", &a);
	printf("0%o %d 0x%x\n", a, a, a);
	return 0;
}
```

# 1669: 求圆的面积

```c
#include<stdio.h>
int main()
{
	float r, mianji;
	scanf("%f", &r);
	mianji = 3.1415926 * r * r;
	printf("%.2f\n", mianji);
	return 0;
}
```

# 1687: 数据结构-字符串连接

```c
#include<stdio.h>
#include<string.h>
int main()
{
	char str1[100], str2[100];
	while(scanf("%s%s", &str1, &str2) != EOF)
	{
		char str[200];
		strcpy(str, str1);
		strcat(str, str2);
		if(strlen(str) > 100)
		{
			printf("Result String is cutted.\n");
		}
		else
		{
			printf("%s\n", str);			
		}
	}
	return 0;
}
```

# 1688: 数据结构-字符串插入

```c
#include<stdio.h>
#include<string.h>

int main()
{
	char str1[128], str2[128];
	int i;
	scanf("%s%s%d", &str1, &str2, &i);
	char str[256];
	int index, count;
	
	//插入str1的前半部分
	for(int j = 0; j < (i - 1); j++)
	{
		str[j] = str1[j];
	}
	
	//插入str2
	index = i - 1;
	count = 0;
	while(count < strlen(str2))
	{
		str[index] = str2[count];
		count ++;
		index ++;
	}
	
	//插入str1的后半部分
	count = i - 1;
	while(count < strlen(str1))
	{
		str[index] = str1[count];
		count++;
		index++;
	}
	str[index] = '\0';
	puts(str);
	return 0;
}
```

# 1806: [编程基础] 输入输出练习之第二个数字
```c
#include<stdio.h>
int main()
{
    int a, b, c;
    scanf("%d%d%d", &a, &b, &c);
	printf("%d\n", b);
	return 0;
}
```

# 1807: [编程基础] 输入输出练习之格式控制
```c
#include<stdio.h>
int main()
{
	int a, b, c;
	scanf("%d%d%d", &a, &b, &c);
	printf("%-8d%-8d%-8d\n", a, b, c);
	return 0;
}
```

# 1808: [编程基础] 输入输出练习之精度控制1
```c
#include<stdio.h>
int main()
{
	float a;
	scanf("%f", &a);
	printf("%.3f\n", a);
	return 0;
}
```

# 1809: [编程基础] 输入输出练习之精度控制2
```c
#include<stdio.h>
int main()
{
	double a;
	scanf("%lf", &a);
	printf("%.12lf\n", a);
	return 0;
}
```

# 1810: [编程基础] 输入输出练习之精度控制3
```c
#include<stdio.h>
int main()
{
	char a;
	int b;
	float c;
	double d;
	scanf("%c%d%f%lf", &a, &b, &c, &d);
	printf("%c %4d %.2f %.12lf\n", a, b, c, d);
	return 0;
}
```

# 1811: [编程基础]输入输出练习之浮点数专题
```c
#include<stdio.h>
int main()
{
	double a;
	scanf("%lf", &a);
	printf("%f\n", a);
	printf("%.5f\n", a);
	printf("%e\n", a);
	printf("%g\n", a);
	return 0;
}
```

# 1812: [编程基础] 输入输出练习之输出图案
```c
#include<stdio.h>
int main()
{
	char c;
	scanf("%c", &c);
	printf("  %c\n", c);
	printf(" %c%c%c\n", c, c, c);
	printf("%c%c%c%c%c\n", c, c, c, c, c);
	return 0;
}
```

# 1833: 蓝桥杯2015年第六届真题-奇怪的数列
```c
#include<stdio.h>
#include<string.h>

int main()
{
	char shuzi[10000];
	gets(shuzi);
	int cishu;
	scanf("%d", &cishu);
	
	while(cishu)
	{
		int len = strlen(shuzi);
		int i = 0, j;
		char next[10000];
		int index = 0;
		while(i < len)
		{
			int count = 0;
			for(j = i; j < len; j++)
			{
				if(shuzi[j] == shuzi[i])
				{
					count++;
				}
				else
				{
					break;
				}
			}
			
			next[index] = (char)(count + 48);
			index++;
			next[index] = shuzi[i];
			index++;
			
			if(count == 1)
			{
				i++;
			}
			else
			{
				i = j;				
			}
		}
		next[index] = '\0';
		strcpy(shuzi, next);
		cishu--;
	}
	puts(shuzi);
	return 0;
}
```

# 1881: 蓝桥杯2017年第八届真题-Excel地址
```c
#include<stdio.h>
int main()
{
	int shuzi;
	scanf("%d", &shuzi);
	char zimu[10000];
	char daxie[26] = {'Z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y'};
	int index = 0;
	while(shuzi)
	{
		zimu[index] = daxie[shuzi % 26];

		if(shuzi % 26 == 0)
		{
			shuzi = shuzi / 26 - 1;
		}
		else
		{
			shuzi = shuzi / 26;
		}
		index++;
	}
	
	for(int i = index - 1; i >= 0; i--)
	{
		if(i == 0)
		{
			printf("%c\n", zimu[i]);
		}
		else
		{
			printf("%c", zimu[i]);			
		}
	}
	
	return 0;
}
```


# 1883: 蓝桥杯2017年第八届真题-日期问题
```c
#include<stdio.h>
int main()
{
	char ymd[8];
	scanf("%s", &ymd);
	
	//a表示第一个数，b表示第二个数，c表示第三个数
	int a = 0, b = 0, c = 0;
	for(int i = 0; i < 8; i++)
	{	
		if(i == 0)
		{
			a = a + ((int)ymd[i] - 48) * 10;
		}
		else if(i == 1)
		{
			a = a + (int)ymd[i] - 48;
		}
		else if(i == 3)
		{
			b = b + ((int)ymd[i] - 48) * 10;
		} 
		else if(i == 4)
		{
			b = b + (int)ymd[i] - 48;
		}
		else if(i == 6)
		{
			c = c + ((int)ymd[i] - 48) * 10;
		}
		else if(i == 7)
		{
			c = c + (int)ymd[i] - 48;
		}
		else
		{
			continue;
		}
	}
	
	int trans[3];
	int count = 0;
	for(int i = 0; i < 3; i++)
	{
		//printf("%d", i);
		int y, m, d;
		if(i == 0) //年月日
		{
			y = a;
			m = b;
			d = c;
		}
		else if(i == 1) //月日年
		{
			m = a;
			d = b;
			y = c;			
		}
		else if(i == 2) //日月年
		{
			d = a;
			m = b;
			y = c;			
		}
		
		//判断年是否满足条件
		if((1900 + y) >= 1960 && (1900 + y) < 2000)
		{
			y = y + 1900;
		}
		else if((2000 + y) >= 2000 && (2000 + y) <= 2059)
		{
			y = y + 2000;
		}
		else
		{
			continue;
		}
					
		//判断月是否在1-12之间
		if(m > 12 || m == 0)
		{
			continue;
		}
				
		//判断日是否正确		
		if(m == 2)  //判断是否满足闰平年2月的天数
		{
			if(y % 400 == 0 || (y % 4 == 0 && y % 100 != 0)) //闰年
			{
				if(d > 29 || d == 0)
				{
					continue;
				}
			}
			else
			{
				if(d > 28 || d == 0)
				{
					continue;
				}
			}
		}
		else if(m == 1 || m == 3 || m == 5 || m == 7 || m == 8 || m == 10 || m == 12)
		{
			if(d > 31 || d == 0)
			{
				continue;
			}
		}
		else
		{
			if(d > 30 || d == 0)
			{
				continue;
			}
		}
		
		
		//去重
		int tmp = y * 10000 + m * 100 + d;
		if(count == 0)
		{
			trans[count] = tmp;
			count++;
		}
		else
		{
			if(tmp != trans[count - 1])
			{
				trans[count] = tmp;
				count++;
			}
		}
	}
	
	if(count == 1)
	{
		printf("%d-%02d-%02d\n", trans[0] / 10000, (trans[0] / 100) % 100, trans[0] % 100);
	}
	else if(count == 2)
	{
		if(trans[0] < trans[1])
		{
			printf("%d-%02d-%02d\n", trans[0] / 10000, (trans[0] / 100) % 100, trans[0] % 100);
			printf("%d-%02d-%02d\n", trans[1] / 10000, (trans[1] / 100) % 100, trans[1] % 100);
		}
		else
		{
			printf("%d-%02d-%02d\n", trans[1] / 10000, (trans[1] / 100) % 100, trans[1] % 100);
			printf("%d-%02d-%02d\n", trans[0] / 10000, (trans[0] / 100) % 100, trans[0] % 100);			
		}	
	}
	else if(count == 3)
	{
		int tmp;
		if(trans[0] > trans[1])
		{
			tmp = trans[0];
			trans[0] = trans[1];
			trans[1] = tmp;
		}
		
		if(trans[1] > trans[2])
		{
			tmp = trans[1];
			trans[1] = trans[2];
			trans[2] = tmp;
		}		

		if(trans[0] > trans[2])
		{
			tmp = trans[0];
			trans[0] = trans[2];
			trans[2] = tmp;
		}
		
		printf("%d-%02d-%02d\n", trans[0] / 10000, (trans[0] / 100) % 100, trans[0] % 100);
		printf("%d-%02d-%02d\n", trans[1] / 10000, (trans[1] / 100) % 100, trans[1] % 100);
		printf("%d-%02d-%02d\n", trans[2] / 10000, (trans[2] / 100) % 100, trans[2] % 100);					
	}
	return 0;
}
```

# 1916: 蓝桥杯算法提高VIP-身份证号码升级
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char yuanshiid[16], shengjiid[18];
	gets(yuanshiid);
	int xishu[17] = {7, 9, 10, 5, 8, 4, 2, 1, 6, 3, 7, 9, 10, 5, 8, 4, 2};
	int sum = 0;
	for(int i = 0; i < 17; i++)
	{
		if(i < 6)
		{
			shengjiid[i] = yuanshiid[i];
		}
		else if(i == 6)
		{
			shengjiid[i] = '1';
		}
		else if(i == 7)
		{
			shengjiid[i] = '9';
		}
		else
		{
			shengjiid[i] = yuanshiid[i - 2];
		}
		sum = sum + (((int)shengjiid[i] - 48) * xishu[i]); 
	}
	int num17;
	num17 = sum % 11;
	if(num17 == 0)
	{
		shengjiid[17] = '1';
	}
	else if(num17 == 1)
	{
		shengjiid[17] = '0'; 
	}
	else if(num17 == 2)
	{
		shengjiid[17] = 'x';
	}
	else if(num17 == 3)
	{
		shengjiid[17] = '9';
	}
	else if(num17 == 4)
	{
		shengjiid[17] = '8';
	}
	else if(num17 == 5)
	{
		shengjiid[17] = '7';
	}
	else if(num17 == 6)
	{
		shengjiid[17] = '6';	
	}
	else if(num17 == 7)
	{
		shengjiid[17] = '5';	
	}
	else if(num17 == 8)
	{
		shengjiid[17] = '4';	
	}
	else if(num17 == 9)
	{
		shengjiid[17] = '3';	
	}
	else if(num17 == 10)
	{
		shengjiid[17] = '2';	
	}
	printf("%s\n", shengjiid);
	return 0;	
}
```

# 1951: 求平方和
```c
#include<stdio.h>
int main()
{
	int a, b;
	int sum;
	scanf("%d%d", &a, &b);
	sum = a * a + b * b;
	printf("%d\n", sum);
	return 0;
}
```

# 1952: 求长方形面积
```c
#include<stdio.h>
int main()
{
	int a, b;
	int c, s;
	scanf("%d%d", &a, &b);
	c = 2 * a + 2 * b;
	s = a * b;
	printf("C:%d\n", c);
	printf("S:%d\n", s);
	return 0;
}
```

# 1954: 话费计算
```c
#include<stdio.h>
int main()
{
	int minutes;
	float cost = 50.0;
	scanf("%d", &minutes);
	cost = cost + 0.4 * minutes;
	printf("%.1f\n", cost);
	return 0;
}
```

# 1955: 贷款计算
```c
#include<stdio.h>
int main()
{
	int loan, months;
	float rate;
	float r;
	scanf("%d%f%d", &loan, &rate, &months);
	loan = loan * 10000;
	r = r + (loan / months) + (loan * rate);
	printf("%.f\n", r);
	return 0;
}
```

# 1980: 求阶梯水费
```c
#include<stdio.h>
int main()
{
	int ysl, money;
	scanf("%d", &ysl);
	if(ysl <= 15)
	{
		money = ysl * 2;
	}
	else
	{
		money = 15 * 2;
		money = money + ((ysl - 15) * 3);
	}
	printf("%d\n", money);
	return 0;	
}
```

# 2001: 边长判断
```c
#include<stdio.h>
int main()
{
	int a, b, c;
	scanf("%d%d%d", &a, &b, &c);
	if (a * a + b * b == c * c || a * a + c * c == b * b || b * b + c * c == a * a)
	{
		printf("YES\n");
	}
	else
	{
		printf("NO\n");
	}
	return 0;	
}
```

# 2002: 计算数字个数
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char s[100];
	gets(s);
	int n;
	n = strlen(s);
	int count = 0;
	for(int i = 0; i < n; i++)
	{
		if (s[i] >= 48 && s[i] <= 57)
		{
			count = count + 1;
		}
	}
	printf("%d\n", count);
	return 0;	
}

```

# 2004: 统计成绩
```c
#include<stdio.h>
#include<string.h>
int main()
{
	int score[10];
	for(int i = 0; i < 10; i++)
	{
		scanf("%d", &score[i]);
	}
	float avg = 0;
	int count = 0;
	for( int i = 0; i < 10; i++)
	{
		avg = avg + score[i];
		if (score[i] < 60)
		{
			count = count + 1;
		}
	}
	avg = avg / 10;
	printf("%.1f %d\n", avg, count);
	return 0;	
}
```

# 2182: [编程入门] 打印图案
```c
#include<stdio.h>
int main()
{
	printf("  *\n");
	printf(" * *\n");
	printf("*****\n");
	return 0;
}
```

# 2194: 蓝桥杯2018年第九届真题-递增三元组
```c
#include<stdio.h>

int main()
{
	int n;
	scanf("%d", &n);
	int a[n], b[n], c[n];
	
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &a[i]);
	}
	
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &b[i]);
	}
	
	for(int i = 0; i < n; i++)
	{
		scanf("%d", &c[i]);
	}
	
	int count = 0;
	for(int i = 0; i < n; i++)
	{
		for(int j = 0; j < n; j++)
		{
			for(int k = 0; k < n; k++)
			{
				if(a[i] < b[j] && b[j] < c[k])
				{
					count++;
				}
			}
		}
	}
	printf("%d\n", count);	
	return 0;
}
```

# 2228: 蓝桥杯算法训练-Anagrams问题
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char str1[81], str2[81];
	gets(str1);
	gets(str2);
	
	int count1[26] = {0}, count2[26] = {0};
	int len1 = strlen(str1);
	int len2 = strlen(str2);
	
	if(len1 != len2)
	{
		printf("N\n");
	}
	else
	{
		for(int i = 0; i < len1; i++)
		{
			if(str1[i] >= 'a' && str1[i] <= 'z')
			{
				count1[(int)(str1[i] - 97)]++;
			}
			
			if(str1[i] >= 'A' && str1[i] <= 'Z')
			{
				count1[(int)(str1[i] - 65)]++;
			}
		}
	
		for(int i = 0; i < len2; i++)
		{
			if(str2[i] >= 'a' && str2[i] <= 'z')
			{
				count2[(int)(str2[i] - 97)]++;
			}
			
			if(str2[i] >= 'A' && str2[i] <= 'Z')
			{
				count2[(int)(str2[i] - 65)]++;
			}
		}
		
		int flag = 1;
		for(int i = 0; i < len1; i++)
		{
			if(count1[i] != count2[i])
			{
				flag = 0;
				break;
			}
		}
		
		if(flag == 1)
		{
			printf("Y\n");
		}		
		else
		{
			printf("N\n");
		}
	}	
	return 0;
}
```

# 2236: 蓝桥杯算法训练-大小写转换
```c
#include<stdio.h>
#include<string.h>
int main()
{
	char str[21];
	gets(str);
	for(int i = 0; i < strlen(str); i++)
	{
		if(str[i] >= 'a' && str[i] <= 'z')
		{
			str[i] = str[i] - 32;
		}
		else
		{
			str[i] = str[i] + 32;
		}
	}
	puts(str);
	return 0;	
}
```

# 2263: 蓝桥杯2015年第六届真题-饮料换购
```c
#include<stdio.h>
int main()
{
	//输入初始拥有的饮料数量
	int n;
	scanf("%d", &n);
	
	//初始化喝饮料的数量，手里攒的瓶盖数
	int hyl = 0, pg = 0;
	
	//开始喝，一瓶一瓶喝
	while(n)
	{
		n--;
		hyl++;
		pg++;
		if(pg == 3)
		{
			n++;
			pg = 0;
		}
	}
	printf("%d\n", hyl);
	return 0;
}
```


# 2266: 蓝桥杯2015年第六届真题-打印大X
```c
#include<stdio.h>
#include<string.h>

int main()
{
	//m表示笔的宽度，n表示大X的高度
	int m, n;
	scanf("%d %d", &m, &n);
	int h = n; //行数
	int z = m + n -1; //列数
	char dax[h][z];
	
	//先将整个二维数组都填满'.'
	for(int i = 0; i < h; i++)
	{
		for(int j = 0; j < z; j++)
		{
			dax[i][j] = '.';
		}
	}
	
	//填充'*'
	for(int i = 0; i < h; i++)
	{
		for(int j = i; j < i + m; j++)
		{
			dax[i][j] = '*';
		}
		
		for(int j = (z - i - 1); j >= (z - i - m); j--)
		{
			dax[i][j] = '*';
		}
	}
	
	//打印
	for(int i = 0; i < h; i++)
	{
		for(int j = 0; j < z; j++)
		{
			if(j == (z - 1))
			{
				printf("%c\n", dax[i][j]);
			}
			else
			{
				printf("%c", dax[i][j]);				
			}
		}
	}
}
```

# 2269: 蓝桥杯2016年第七届真题-冰雹数
```c
#include<stdio.h>
int main()
{
	long long n;
	scanf("%ld", &n);
	long long max = 1;
	long long i;
	for(i = 1; i <= n; i++)
	{
		long long num = i;
		while(num != 1)
		{
			if(num % 2 == 0) //偶数 
			{
				num = num / 2;
			}
			else //奇数 
			{
				num = num * 3 + 1; 
			} 
			if(num > max)
			{
				max = num;
			}
		}
	}
	printf("%ld\n", max);
	return 0;
} 
```

# 2281: 蓝桥杯2018年第九届真题-次数差
```c
#include<stdio.h>
#include<string.h>

int main()
{
	char bisai[1000];
	int cishu[26] = {0};
	scanf("%s", &bisai);
	int len = strlen(bisai);
	int max = 0, min = 1000;
	for(int i = 0; i < len; i++)
	{
		cishu[(int)(bisai[i] - 'a')]++;
	}
	
	for(int i = 0; i < 26; i++)
	{
		if(cishu[i] !=0 )
		{
			if(cishu[i] > max)
			{
				max = cishu[i];
			}
		
			if(cishu[i] < min)
			{
				min = cishu[i];
			}
		}
	}
	
	printf("%d\n", max - min);
	return 0;
}
```

# 2308: 蓝桥杯2019年第十届省赛真题-旋转
```c
#include<stdio.h>
int main()
{
	int m, n;
	scanf("%d%d", &m, &n);
	
	int tupian[m][n];
	for(int i = 0; i < m; i++)
	{
		for(int j = 0; j < n; j++)
		{
			scanf("%d", &tupian[i][j]);
		}
	}
	
	int m_xz = n;
	int n_xz = m;
	int tupian_xz[m_xz][n_xz];
	
	for(int i = 0; i < n_xz; i++)
	{
		for(int j = 0; j < m_xz; j++)
		{
			tupian_xz[j][i] = tupian[m - i - 1][j];
		}
	}
	
	for(int i = 0; i < m_xz; i++)
	{
		for(int j = 0; j < n_xz; j++)
		{
			if(j == n_xz - 1)
			{
				printf("%d\n", tupian_xz[i][j]);
			}
			else
			{
				printf("%d ", tupian_xz[i][j]);
			}
		}
	}
	return 0;
}
```

# 2620: 蓝桥杯2021年第十二届国赛真题-大写
```c
#include<stdio.h>
#include<string.h>

int main()
{
	char str[1000];
	gets(str);
	int len = strlen(str);
	for(int i = 0; i < len; i++)
	{
		if(str[i] >= 'a' && str[i] <= 'z')
		{
			str[i] = str[i] - 32;
		}
	}
	puts(str);
	return 0;
}
```
