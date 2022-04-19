# 1. A + B
```cpp
#include<iostream>
using namespace std;
int main()
{
    int a, b;
    cin >> a >> b;
    cout << a + b <<endl;
    return 0;
}
```

# 466. 回文日期
**最开始想到的思路，但是下面这种方式会超时。**
```cpp
#include<iostream>
#include<string>
using namespace std;

//判断回文
bool check_huiwen(long date)
{
    string s = to_string(date);
    int i, j;
    bool is_huiwen = true;
    for(i = 0, j = s.length() - 1; i < j; i++, j--)
    {
        if(s[i] != s[j])
        {
            is_huiwen = false;
            break;
        }
    }
    return is_huiwen;
}

//判断日期是否合法
bool check_date(long date)
{
    int days[13] = {0, 31, 30, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};

    //获取年月日
    int year, month, day;
    year = date / 10000;
    month = date % 10000 / 100;
    day = date % 100; 

    //判断"月"是否合法
    if(month > 12 || month < 1)
    {
        return false;
    }

    //判断除了2月以外的月"天"是否合法
    if(month !=2 && day > days[month])
    {
        return false;
    }

    //判断2月的"天"是否合法
    if(month == 2)
    {
        //闰年
        if((year % 4 == 0 && year % 100 != 0) || year % 400 == 0)
        {
            if(day > 29)
            {
                return false;
            }
        }
        else //平年
        {
            if(day > 28)
            {
                return false;
            }
        }
    }
    return true;
}


int main()
{
    long date1, date2;
    cin >> date1 >> date2;
    int count = 0;
    for(long i = date1; i <= date2; i++)
    {
        if(check_date(i))
        {
            if(check_huiwen(i))
            {
                count++;
            }
        }    
    }

    cout << count << endl;
    return 0;
}
```

# 604. 圆的面积 
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	double pi, r, s;
	cin >> r;
	pi = 3.14159;
	s = pi * r * r;
	printf("A=%.4lf\n", s);
	return 0;
}
```

# 605. 简单乘积
```cpp
#include<iostream>
using namespace std;
int main()
{
	int a, b, x;
	cin >> a >> b;
	x = a * b;
	cout << "PROD = " << x << endl;
	return 0;
}
```

# 606. 平均数1
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	double a, b, avg;
	cin >> a;
	cin >> b;
	avg = a * 3.5 / 11 + b * 7.5 / 11;
	printf("MEDIA = %.5lf\n", avg);
	return 0;
}
```

# 607. 平均数2
```cpp
#include<iostream>
#include<cstdio>
#include<cmath>
using namespace std;
int main()
{
	double a, b, c, avg;
	cin >> a >> b >> c;
	avg = a * 0.2 + b * 0.3 + c * 0.5;
	printf("MEDIA = %.1lf\n", avg);
	return 0;
}
```

# 608. 差
```cpp
#include<iostream>
using namespace std;
int main()
{
    int a, b, c, d;
    cin >> a >> b >> c >> d;
    cout << "DIFERENCA = " << (a * b - c * d) << endl;
    return 0;
}
```

# 609. 工资
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	int no, length;
	double hour_salary, salary;
	cin >> no >> length >> hour_salary;
	cout << "NUMBER = " << no << endl;
	salary = hour_salary * length;
	printf("SALARY = U$ %.2lf\n", salary);
	return 0;
}
```


# 610. 工资和奖金
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	string name;
	double dixin, xiaoshoue;
	cin >> name >> dixin >> xiaoshoue;
	double yueshouru;
	yueshouru = dixin + xiaoshoue * 0.15;
	printf("TOTAL = R$ %.2lf\n", yueshouru);
	return 0;
}
```

# 611. 简单计算
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	int bianhao1, shuliang1, bianhao2, shuliang2;
	double danjia1, danjia2;
	cin >> bianhao1 >> shuliang1 >> danjia1 >> bianhao2 >> shuliang2 >> danjia2;
	double zongjia = shuliang1 * danjia1 + shuliang2 * danjia2;
	printf("VALOR A PAGAR: R$ %.2lf\n", zongjia); 
	return 0;
}
```

# 612. 球的体积
```cpp
#include<iostream>
#include<cstdio>
#include<cmath>
using namespace std;
int main()
{
	double r;
	cin >> r;
	double volume;
	double pi = 3.14159;
	volume = (4.0 / 3.0) * pi * pow(r, 3);
	printf("VOLUME = %.3lf\n", volume);  
	return 0;
}
```

# 613. 面积
```cpp
#include<iostream>
#include<cstdio>
#include<cmath>
using namespace std;
int main()
{
	double a, b, c, pi = 3.14159;
	cin >> a >> b >> c;
	double s1, s2, s3, s4, s5;
	s1 = 0.5 * a * c;
	s2 = pi * pow(c, 2);
	s3 = (a + b) * c * 0.5;
	s4 = pow(b, 2);
	s5 = a * b;
	printf("TRIANGULO: %.3lf\n", s1); 
	printf("CIRCULO: %.3lf\n", s2);
	printf("TRAPEZIO: %.3lf\n", s3);
	printf("QUADRADO: %.3lf\n", s4);
	printf("RETANGULO: %.3lf\n", s5);
	return 0;
}
```

# 614. 最大值
```cpp
#include<iostream>
#include<cstdio>
#include<cmath>
using namespace std;
int main()
{
	int x1, x2, x3;
	int max_value;
	cin >> x1 >> x2 >> x3;
	max_value = (x1 + x2 + abs(x1 - x2)) * 0.5;
	max_value = (x3 + max_value + abs(x3 - max_value)) * 0.5;
	printf("%d eh o maior\n", max_value);
	return 0;
}
```

# 615. 油耗
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	double km, fuel;
	cin >> km >> fuel;
	printf("%.3lf km/l\n", km / fuel);
	return 0;
}
```

# 616. 两点间的距离
```cpp
#include<iostream>
#include<cstdio>
#include<cmath>
using namespace std;
int main()
{
	double x1, y1, x2, y2, dist;
	cin >> x1 >> y1 >> x2 >> y2;
	dist = sqrt(pow((x2- x1), 2) + pow((y2 - y1), 2));
	printf("%.4lf\n", dist);
	return 0;
}
```

# 617. 距离
```cpp
#include<iostream>
using namespace std;
int main()
{
	int km;
	cin >> km;
	cout << km * 2 << " minutos" << endl;
	return 0;
}
```

# 618. 燃料消耗
```cpp
#include<iostream>
using namespace std;
int main()
{
	long long t, v;
	cin >> t >> v;
	double fuel;
	fuel = v * t / 12.0;
	printf("%.3lf\n", fuel);
	return 0;
}
```

# 653. 钞票
```cpp
#include<iostream>
#include<cstring>
using namespace std;
int main()
{
	int total;
	cin >> total;
	int cp_mianzhi[7] = {100, 50, 20, 10, 5, 2, 1};
	int cp_shuliang[7];
	memset(cp_shuliang, 0, sizeof cp_shuliang);
	int number = total;
	for(int i = 0; i < 7; i++)
	{
		if(number >= cp_mianzhi[i])
		{
			cp_shuliang[i] = number / cp_mianzhi[i];
			number = number % cp_mianzhi[i];
		}
		else
		{
			continue;
		}
	}
	cout << total << endl;
	for(int i = 0; i < 7; i++)
	{
		cout << cp_shuliang[i] << " nota(s) de R$ " << cp_mianzhi[i] << ",00" << endl;
	}
	return 0;
}
```

# 654. 时间转换
```cpp
#include<iostream>
using namespace std;
int main()
{
	int total;
	cin >> total;
	int hours, minutes, seconds;
	hours = total / 3600;
	minutes = total % 3600 / 60;
	seconds = total % 3600 % 60;
	cout << hours << ":" << minutes << ":" << seconds << endl;
	return 0;
}
```

# 655. 天数转换
```cpp
#include<iostream>
using namespace std;
int main()
{
	int days;
	cin >> days;
	cout << days / 365 << " ano(s)" << endl;
	cout << days % 365 / 30 << " mes(es)" << endl;
	cout << days % 365 % 30 << " dia(s)" << endl;
	return 0;
}
```

# 656. 钞票和硬币
```cpp
#include<iostream>
#include<cmath>
#include<cstring>
#include<cstdio>
using namespace std;
int main()
{
	double total;
	cin >> total;
	double cpmz[6] = {100.0, 50.0, 20.0, 10.0, 5.0, 2.0};
	double ybmz[6] = {1, 0.5, 0.25, 0.1, 0.05, 0.01};
	int cpsl[6], ybsl[6];
	memset(cpsl, 0, sizeof cpsl);
	memset(ybsl, 0, sizeof ybsl);
	
	double number = total;
	for(int i = 0; i < 6; i++)
	{
		if(number > cpmz[i] || abs(number - cpmz[i]) < 0.0000001)
		{
			cpsl[i] = floor(number / cpmz[i]);
			number = number - cpmz[i] * cpsl[i];
		}
		else
		{
			continue;
		}
	}
	
	for(int i = 0; i < 6; i++)
	{
		if(number > ybmz[i] || abs(number - ybmz[i]) < 0.000001) 
		{
			ybsl[i] = floor((number + 0.000001) / ybmz[i]);
			number = number - ybmz[i] * ybsl[i];
		}
		else
		{
			continue;
		}
	}
	
	cout << "NOTAS:" << endl;
	for(int i = 0; i < 6; i++)
	{
		printf("%d nota(s) de R$ %.2lf\n", cpsl[i], cpmz[i]);
	}
	cout << "MOEDAS:" << endl;
	for(int i = 0; i < 6; i++)
	{
		printf("%d moeda(s) de R$ %.2lf\n", ybsl[i], ybmz[i]);
	}	
	return 0;
}
```

# 657. 选择练习1
```cpp
#include<iostream>
using namespace std;
int main()
{
	int a, b, c, d;
	cin >> a >> b >> c >> d;
	if(b > c && d > a && (c + d) > (a + b) && c > 0 && d > 0 && a % 2 == 0)
	{
		cout << "Valores aceitos" << endl;
	}	
	else
	{
		cout << "Valores nao aceitos" << endl;
	}
	return 0;
}
```

# 658. 一元二次方程公式
```cpp
#include<iostream>
#include<cmath>
#include<cstdio>
using namespace std;
int main()
{
	double a, b, c;
	cin >> a >> b >> c;
	if(a == 0 || (pow(b, 2) - 4 * a * c) < 0)
	{
		cout << "Impossivel calcular" << endl;
	}
	
	double x1, x2;
	x1 = (-1 * b + sqrt(pow(b, 2) - 4 * a * c)) / (2 * a);
	x2 = (-1 * b - sqrt(pow(b, 2) - 4 * a * c)) / (2 * a);
	
	printf("R1 = %.5lf\n", x1);
	printf("R2 = %.5lf\n", x2);	
	return 0;
}
```


# 659. 区间
```cpp
#include<iostream>
using namespace std;
int main()
{
	double x;
	cin >> x;
	if(x < 0 || x > 100)
	{
		cout << "Fora de intervalo" << endl;
	}
	else if(x >= 0 && x <= 25)
	{
		cout << "Intervalo [0,25]" << endl;
	}
	else if(x > 25 && x <= 50)
	{
		cout << "Intervalo (25,50]" << endl;
	}
	else if(x > 50 && x <= 75)
	{
		cout << "Intervalo (50,75]" << endl;
	}
	else if(x > 75 && x <= 100)
	{
		cout << "Intervalo (75,100]" << endl;
	}
	return 0;
}
```

# 660. 零食
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	double snack[5] = {4.00, 4.50, 5.00, 2.00, 1.50};
	int no, number;
	cin >> no >> number;
	printf("Total: R$ %.2lf\n", snack[no - 1] * number); 
	return 0;
}
```

# 661. 平均数3
```cpp
#include<iostream>
#include<cmath>
#include<cstdio>
using namespace std;
int main()
{
	double n1, n2, n3, n4;
	cin >> n1 >> n2 >> n3 >> n4;
	double avg;
	avg = n1 * 0.2 + n2 * 0.3 + n3 * 0.4 + n4 * 0.1;
	printf("Media: %.1lf\n", avg);
	if(avg >= 7.0)
	{
		cout << "Aluno aprovado." << endl;
	}
	else if(avg < 5.0)
	{
		cout << "Aluno reprovado." << endl;
	}
	else if(avg >= 5.0 && avg < 7.0)
	{
		cout << "Aluno em exame." << endl;
		double y;
		cin >> y;
		printf("Nota do exame: %.1lf\n", y);
		double avg2;
		avg2 = (avg + y) * 0.5;
		if(avg2 >= 5.0)
		{
			cout << "Aluno aprovado." << endl;
		}
		else
		{
			cout << "Aluno reprovado." << endl;
		}
		printf("Media final: %.1lf\n", avg2);
	}
	return 0;
}
```

# 662. 点的坐标
```cpp
#include<iostream>
using namespace std;
int main()
{
	double x, y;
	cin >> x >> y;
	if(x > 0 && y > 0)
	{
		cout << "Q1" << endl;
	}
	else if(x < 0 && y > 0)
	{
		cout << "Q2" << endl;
	}
	else if(x < 0 && y < 0)
	{
		cout << "Q3" << endl;
	}
	else if(x > 0 && y < 0)
	{
		cout << "Q4" << endl;
	}
	else if(y == 0 && x != 0)
	{
		cout << "Eixo X" << endl;
	}
	else if(x == 0 && y != 0)
	{
		cout << "Eixo Y" << endl;
	}
	else if(x ==0 && y == 0)
	{
		cout << "Origem" << endl;
	}
	return 0;
}
```

# 663. 简单排序
```cpp
#include<iostream>
using namespace std;
int main()
{
	int a_old, b_old, c_old;
	cin >> a_old >> b_old >> c_old;
	
	int a_new, b_new, c_new;
	a_new = a_old;
	b_new = b_old;
	c_new = c_old;
	
	int temp;
	if(a_new > b_new)
	{
		temp = a_new;
		a_new = b_new;
		b_new = temp;
	}
	
	if(a_new > c_new)
	{
		temp = a_new;
		a_new = c_new;
		c_new = temp;
	}
	
	if(b_new > c_new)
	{
		temp = b_new;
		b_new = c_new;
		c_new = temp;
	}
	
	cout << a_new << endl;
	cout << b_new << endl;
	cout << c_new << endl;
	cout << endl;
	cout << a_old << endl;
	cout << b_old << endl;
	cout << c_old << endl;	
	return 0;
}
```

# 664. 三角形
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	double a, b, c;
	cin >> a >> b >> c;
	if((a + b) > c && (a + c) > b && (b + c) > a)
	{
		printf("Perimetro = %.1lf\n", a + b + c);
	}
	else
	{
		printf("Area = %.1lf\n", (a + b) * c * 0.5);
	}
	return 0;
}
```

# 665. 倍数
```cpp
#include<iostream>
using namespace std;
int main()
{
	int a, b;
	cin >> a >> b;
	if(a % b == 0 || b % a == 0)
	{
		cout << "Sao Multiplos" << endl;
	}
	else
	{
		cout << "Nao sao Multiplos" << endl;
	}
	return 0;
}
```

# 666. 三角形类型
```cpp
#include<iostream>
#include<cmath>
using namespace std;
int main()
{
	double a, b, c;
	cin >> a >> b >> c;
	double tmp;
	if(a < b)
	{
		tmp = a;
		a = b;
		b = tmp;
	}

	if(a < c)
	{
		tmp = a;
		a = c;
		c = tmp;
	}
		
	if(b < c)
	{
		tmp = b;
		b = c;
		c = tmp;
	}
	

	
	if(a >= (b + c))
	{
		cout << "NAO FORMA TRIANGULO" << endl;
	}
	else
	{
		if(pow(a, 2) == (pow(b, 2) + pow(c, 2)))
		{
			cout << "TRIANGULO RETANGULO" << endl;
		}
		if(pow(a, 2) > (pow(b, 2) + pow(c, 2)))
		{
			cout << "TRIANGULO OBTUSANGULO" << endl;
		}
		if(pow(a, 2) < (pow(b, 2) + pow(c, 2)))
		{
			cout << "TRIANGULO ACUTANGULO" << endl;
		}
		if(a == b && b == c && a == c)
		{
			cout << "TRIANGULO EQUILATERO" << endl;
		}
		if((a == b && b != c) || (a == c && c != b) || (b == c && a != c))
		{
			cout << "TRIANGULO ISOSCELES" << endl;
		}
	}
	return 0;
}
```

# 667. 游戏时间
```cpp
#include<iostream>
using namespace std;
int main()
{
	int start_time, end_time;
	cin >> start_time >> end_time;
	int duration;
	if(start_time > end_time)
	{
		duration = 24 - start_time + end_time;
	}
	else if(start_time == end_time)
	{
		duration = 24;
	}
	else if(start_time < end_time)
	{
		duration = end_time - start_time;
	}
	cout << "O JOGO DUROU " << duration << " HORA(S)" << endl;
	return 0;
}
```

# 668. 游戏时间2
```cpp
#include<iostream>
#include<cmath>
using namespace std;
int main()
{
	int start_hour, start_minute, end_hour, end_minute;
	cin >> start_hour >> start_minute >> end_hour >> end_minute;
	int duration_hour, duration_minute;

	if(start_hour == end_hour && start_minute >= end_minute) //计算小时间隔
	{
		duration_hour = 24;
	}
	else if(start_hour > end_hour)
	{
		duration_hour = 24 - start_hour + end_hour;
	}
	else
	{
		duration_hour = end_hour - start_hour;
	}
	
	if(start_minute == end_minute) //计算分钟间隔
	{
		duration_minute = 0;
	}
	else if(start_minute > end_minute)
	{
		duration_minute = 60 - start_minute + end_minute;
		duration_hour = duration_hour - 1;
	}
	else
	{
		duration_minute = end_minute - start_minute;
	}
	cout << "O JOGO DUROU " << duration_hour << " HORA(S) E " << duration_minute << " MINUTO(S)" << endl;
	return 0;
}
```

# 669. 加薪
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	double salary_old, salary_new, add_value;
	int fudu;
	cin >> salary_old;
	if(salary_old > 0 && salary_old <= 400.00)
	{
		add_value = salary_old * 0.15;
		fudu = 15;
	}
	else if(salary_old >= 400.01 && salary_old <= 800.00)
	{
		add_value = salary_old * 0.12;
		fudu = 12;
	}
	else if(salary_old >= 800.01 && salary_old <= 1200.00)
	{
		add_value = salary_old * 0.1;
		fudu = 10;
	}
	else if(salary_old >= 1200.01 && salary_old <= 2000.00)
	{
		add_value = salary_old * 0.07;
		fudu = 7;
	}
	else if(salary_old > 2000)
	{
		add_value = salary_old * 0.04;
		fudu = 4;
	}
	salary_new = salary_old + add_value;
	printf("Novo salario: %.2lf\n", salary_new);
	printf("Reajuste ganho: %.2lf\n", add_value);
	printf("Em percentual: %d \%\n", fudu);
	return 0;
}
```

# 670. 动物
```cpp
#include<iostream>
using namespace std;
int main()
{
	string a, b, c;
	cin >> a >> b >> c;
	if(a == "vertebrado" && b == "ave" && c == "carnivoro")
	{
		cout << "aguia" << endl;
	}
	else if(a == "vertebrado" && b == "ave" && c == "onivoro")
	{
		cout << "pomba" << endl;
	}
	else if(a == "vertebrado" && b == "mamifero" && c == "onivoro")
	{
		cout << "homem" << endl;
	}
	else if(a == "vertebrado" && b == "mamifero" && c == "herbivoro")
	{
		cout << "vaca" << endl;
	}
	else if(a == "invertebrado" && b == "inseto" && c == "hematofago")
	{
		cout << "pulga" << endl;
	}
	else if(a == "invertebrado" && b == "inseto" && c == "herbivoro")
	{
		cout << "lagarta" << endl;
	}
	else if(a == "invertebrado" && b == "anelideo" && c == "hematofago")
	{
		cout << "sanguessuga" << endl;
	}
	else if(a == "invertebrado" && b == "anelideo" && c == "onivoro")
	{
		cout << "minhoca" << endl;
	}	
	return 0;
}
```

# 671. DDD
```cpp
#include<iostream>
using namespace std;
int main()
{
	int a;
	cin >> a;
	if(a == 61)
	{
		cout << "Brasilia" << endl;
	}
	else if(a == 71)
	{
		cout << "Salvador" << endl;
	}
	else if(a == 11)
	{
		cout << "Sao Paulo" << endl;
	}
	else if(a == 21)
	{
		cout << "Rio de Janeiro" << endl;
	}
	else if(a == 32)
	{
		cout << "Juiz de Fora" << endl;
	}
	else if(a == 19)
	{
		cout << "Campinas" << endl;
	}
	else if(a == 27)
	{
		cout << "Vitoria" << endl;
	}
	else if(a == 31)
	{
		cout << "Belo Horizonte" << endl;
	}
	else
	{
		cout << "DDD nao cadastrado" << endl;
	}
	return 0;
}
```

# 672. 税
```cpp
#include<iostream>
#include<cstdio>
using namespace std;
int main()
{
	double salary;
	cin >> salary;
	double taxes;
	if(salary >= 0.00 && salary <= 2000.00)
	{
		cout << "Isento" << endl;
	}
	else
	{
		if(salary >= 2000.01 && salary <= 3000.00)
		{
			taxes = (salary - 2000.00) * 0.08;
		}
		else if(salary >= 3000.01 && salary <= 4500)
		{
			taxes = 1000.00 * 0.08;
			taxes = taxes + (salary - 3000.00) * 0.18;
		}
		else if(salary > 4500.00)
		{
			taxes = 1000.00 * 0.08;
			taxes = taxes + 1500 * 0.18;
			taxes = taxes + (salary - 4500) * 0.28;
		}
		printf("R$ %.2lf\n", taxes);
	}
	return 0;
}
```

# 708. 偶数
```cpp
#include<iostream>
using namespace std;
int main()
{
	for(int i = 1; i <= 100; i++)
	{
		if(i % 2 == 0)
		{
			cout << i << endl;
		}
	}
	return 0;
}
```

# 709. 奇数
```cpp
#include<iostream>
using namespace std;
int main()
{
	int x;
	cin >> x;
	for(int i = 1; i <= x; i++)
	{
		if(i % 2 != 0)
		{
			cout << i << endl;
		}
	}
	return 0;
}
```

# 710. 六个奇数
```cpp
#include<iostream>
using namespace std;
int main()
{
	int x, cnt = 0;
	cin >> x;
	if(x % 2 != 0)
	{
		cout << x << endl;
		cnt ++;
	}
	while(cnt < 6)
	{
		x = x + 1;
		if(x % 2 != 0)
		{
			cout << x << endl;
			cnt ++;
		}
	}
	return 0;
}
```

# 711. 乘法表
```cpp
#include<iostream>
using namespace std;
int main()
{
	int n;
	cin >> n;
	for(int i = 1; i <= 10; i++)
	{
		cout << i << " x " << n << " = " << i * n << endl; 
	}
	return 0;
}
```


# 712. 正数
```cpp
#include<iostream>
using namespace std;
int main()
{
	double x;
	int cnt = 0;
	for(int i = 0; i < 6; i++)
	{
		cin >> x;
		if(x > 0)
		{
			cnt ++;
		}
	}
	cout << cnt << " positive numbers" << endl;
	return 0;
}
```

# 713. 区间2
```cpp
#include<iostream>
using namespace std;

int main()
{
	int n;
	cin >> n;
	int x, cnt_in = 0, cnt_out = 0;
	for(int i = 0; i < n; i++)
	{
		cin >> x;
		if(x >= 10 && x <= 20)
		{
			cnt_in ++;
		}
		else
		{
			cnt_out ++;
		} 
	}
	cout << cnt_in << " in" << endl;
	cout << cnt_out << " out" << endl;
	return 0;
}
```

# 714. 连续奇数的和1
```cpp
#include<iostream>
using namespace std;
int main()
{
	int x, y;
	cin >> x >> y;
	int sum = 0;
	int temp;
	if(x > y)
	{
		temp = x;
		x = y;
		y = temp;
	}
	for(int i = x + 1; i < y; i++)
	{
		if(i % 2 != 0)
		{
			sum = sum + i;
		}
	}
	cout << sum << endl;
	return 0;
}
```

# 715. 余数
```cpp
#include<iostream>
using namespace std;
int main()
{
	int n;
	cin >> n;
	for(int i = 2; i < 10000; i++)
	{
		if(i % n == 2)
		{
			cout << i << endl;
		}
	}
	return 0;
}
```

# 716. 最大数和它的位置
```cpp
#include<iostream>
using namespace std;
int main()
{
	int x;
	int max_index, max_value;
	for(int i = 1; i <= 100; i++)
	{
		cin >> x;
		if(i == 1)
		{
			max_index = 1;
			max_value = x;
		}
		else
		{
			if(x > max_value)
			{
				max_index = i;
				max_value = x;
			}
		}
	}
	cout << max_value << endl;
	cout << max_index << endl;
	return 0;
}
```

# 717. 简单斐波那契
```cpp
#include<iostream>
using namespace std;

int main()
{
	int n;
	cin >> n;
	int fbnq[46];
	fbnq[0] = 0;
	fbnq[1] = 1;
	for(int i = 2; i < 46; i++)
	{
		fbnq[i] = fbnq[i - 2] + fbnq[i - 1];
	}
	
	for(int i = 0; i < n; i++)
	{
		if(i == n - 1)
		{
			cout << fbnq[i] << endl;
		}
		else
		{
			cout << fbnq[i] << " ";
		}
	}
	return 0;
}
```

# 718. 实验
```cpp
#include<iostream>
#include<cstdio>
using namespace std;

int main()
{
	int n;
	cin >> n;
	int total = 0, total_c = 0, total_r = 0, total_f = 0;
	for(int i = 0; i < n; i++)
	{
		int a;
		char c;
		cin >> a >> c;
		if(c == 'C')
		{
			total_c = total_c + a;
		}
		else if(c == 'R')
		{
			total_r = total_r + a;
		}
		else if(c == 'F')
		{
			total_f = total_f + a;
		}
		total = total + a;
	}
	
	cout << "Total: " << total << " animals" << endl;
	cout << "Total coneys: " << total_c << endl;
	cout << "Total rats: " << total_r << endl;
	cout << "Total frogs: " << total_f << endl;
	printf("Percentage of coneys: %.2lf %\n", ((double)total_c / total) * 100);
	printf("Percentage of rats: %.2lf %\n", ((double)total_r / total) * 100);
	printf("Percentage of frogs: %.2lf %\n", ((double)total_f / total) * 100);	
	return 0;
}
```

# 719. 连续奇数的和2
```cpp
#include<iostream>
using namespace std;

int main()
{
	int n;
	cin >> n;
	for(int i = 0; i < n; i++)
	{
		int x, y;
		cin >> x >> y;
		if(x > y)
		{
			int temp;
			temp = x;
			x = y;
			y = temp;
		}
		int odd_sum = 0;
		for(int j = x + 1; j < y; j++)
		{
			if(j % 2 != 0)
			{
				odd_sum = odd_sum + j;
			}
		}
		cout << odd_sum << endl;
	}
	return 0;
}
```

# 720. 连续整数相加
```cpp
#include<iostream>
using namespace std;
int main()
{
	int a, n;
	cin >> a;
	cin >> n;
	while(n <= 0)
	{
		cin >> n;
	}
	int sum = 0;
	for(int i = 0; i < n; i++)
	{
		sum = sum + a + i;
	}
	cout << sum << endl;
	return 0;
}
```

# 721. 递增序列
```cpp
#include<iostream>
using namespace std;
int main()
{
	int x;
	cin >> x;
	while(x != 0)
	{
		for(int i = 1; i <= x; i++)
		{
			if(i == x)
			{
				cout << i << endl;
			}
			else
			{
				cout << i << " ";
			}
		}
		cin >> x;
	}
	return 0;
}
```

# 722. 数字序列和它的和
```cpp
#include<iostream>
using namespace std;

int main()
{
	int m, n;
	cin >> m >> n;
	while(m > 0 && n > 0)
	{
		if(m > n)
		{
			int temp;
			temp = m;
			m = n;
			n = temp;
		}
		int sum = 0;
		for(int i = m; i <= n; i++)
		{
			sum = sum + i;
			cout << i << " ";
		}
		cout << "Sum=" << sum << endl;
		cin >> m >> n;
	}
	return 0;
}
```

# 723. PUM
```cpp
#include<iostream>
using namespace std;
int main()
{
	int n, m;
	cin >> n >> m;
	for(int i = 1; i <= n * m; i++)
	{
		if(i % m == 0)
		{
			cout << "PUM" << endl;
		}
		else
		{
			cout << i << " ";
		}
	}
	return 0;
}
```

# 724. 约数
```cpp
#include<iostream>
using namespace std;
int main()
{
	int n;
	cin >> n;
	for(int i = 1; i <= n; i++)
	{
		if(n % i == 0)
		{
			cout << i << endl;
		}
	}
	return 0;
}
```

# 725. 完全数
```cpp
#include<iostream>
#include<cmath>
using namespace std;

int main()
{
	int n;
	cin >> n;
	for(int i = 0; i < n; i++)
	{
		int x;
		cin >> x;
		int yue_sum = 1;
		for(int j = 2; j < sqrt(x); j++)
		{
			if(x % j == 0)
			{
				yue_sum = yue_sum + j + x / j;
			}
		}
		if(x == yue_sum && x!= 1)
		{
			cout << x << " is perfect" << endl;
		}
		else
		{
			cout << x << " is not perfect" << endl;
		}
	}
	return 0;
}
```

# 726. 质数
```cpp
#include<iostream>
#include<cmath>
using namespace std;

int main()
{
	int n;
	cin >> n;
	for(int i = 0; i < n; i++)
	{
		int x;
		cin >> x;
		int flag = 1;
		for(int j = 2; j < x; j++)
		{
			if(x % j == 0)
			{
				flag = 0;
				break;
			}
		}
		if(flag == 0)
		{
			cout << x << " is not prime" << endl;
		}
		else
		{
			cout << x << " is prime" << endl;
		}
	}
	return 0;
}
```

# 727. 菱形
```cpp
#include<iostream>
#include<cmath>
using namespace std;

int main()
{
	int n;
	cin >> n;
	char lingxing[n][n];
	for(int i = 0; i < n; i++)
	{
		for(int j = 0; j < n; j++)
		{
			lingxing[i][j] = '*';
		}
	}
	
	
	for(int i = 0; i < n; i++)
	{
		int space_number = abs(n / 2 - i);
		int p, q;
		for(p = 0, q = n - 1; p != q; p++, q--)
		{
			if(space_number != 0)
			{
				lingxing[i][p] = ' ';
				lingxing[i][q] = ' ';
				space_number --;
			}	
		}
	}
	
	for(int i = 0; i < n; i++)
	{
		for(int j = 0; j < n; j++)
		{
			if(j == n - 1)
			{
				cout << lingxing[i][j] << endl;
			}
			else
			{
				cout << lingxing[i][j];				
			}
		}
	}	
	return 0;
}
```

# 737. 数组替换
```cpp
#include<iostream>
using namespace std;

int main()
{
	int x[10];
	for(int i = 0; i < 10; i++)
	{
		cin >> x[i];
		if(x[i] <= 0)
		{
			x[i] = 1;
		}
	}
	
	for(int i = 0; i < 10; i++)
	{
		cout << "X[" << i << "] = " << x[i] << endl;
	}
	
	return 0;
}
```

# 738. 数组填充
```cpp
#include<iostream>
using namespace std;

int main()
{
	int v;
	cin >> v;
	int n[10];
	n[0] = v;
	for(int i = 1; i < 10; i++)
	{
		n[i] = 2 * n[i - 1];
	}
	for(int i = 0; i < 10; i++)
	{
		cout << "N[" << i << "] = " << n[i] << endl;
	}	
	return 0;
}
```

# 739. 数组选择
```cpp
#include<iostream>
using namespace std;

int main()
{
	double a[100];
	for(int i = 0; i < 100; i++)
	{
		cin >> a[i];
	}
	for(int i = 0; i < 100; i++)
	{
		if(a[i] <= 10)
		{
			printf("A[%d] = %.1lf\n", i, a[i]); 
		}
	}
	return 0;
}
```

# 740. 数组变换
```cpp
#include<iostream>
#include<cmath>
using namespace std;

int main()
{
	int num[20];
	for(int i = 0; i < 20; i++)
	{
		cin >> num[i];
	}
	
	for(int i = 19; i >= 0; i--)
	{
		cout << "N[" << abs(i - 19) << "] = " << num[i] << endl;
	}
	return 0;
}
```

# 741. 斐波那契数列
```cpp
#include<iostream>
using namespace std;

int main()
{
	long long fbnq[60];
	fbnq[0] = 0;
	fbnq[1] = 1;
	for(int i = 2; i < 60; i++)
	{
		fbnq[i] = fbnq[i - 1] + fbnq[i - 2];
	}
	int n;
	cin >> n;
	for(int i = 0; i < n; i++)
	{
		int num;
		cin >> num;
		cout << "Fib(" << num << ") = " << fbnq[num] << endl; 
	}
	return 0;
}
```

# 742. 最小数和它的位置
```cpp
#include<iostream>
using namespace std;

int main()
{
	int n;
	cin >> n;
	int num[n];
	for(int i = 0; i < n; i++)
	{
		cin >> num[i];
	}
	int min_value = num[0];
	int min_index = 0;
	
	for(int i = 1; i < n; i++)
	{
		if(num[i] < min_value)
		{
			min_value = num[i];
			min_index = i;
		}
		else if(num[i] == min_value)
		{
			if(i < min_index)
			{
				min_index = i;
			}
		}
	}
	cout << "Minimum value: " << min_value << endl;
	cout << "Position: " << min_index << endl;
	return 0;
}
```

# 743. 数组中的行
```cpp
#include<iostream>
using namespace std;

int main()
{
	int l;
	cin >> l;
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	double sum = 0.0;
	for(int i = 0; i < 12; i++)
	{
		sum = sum + m[l][i];
	}
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else if(c == 'M')
	{
		printf("%.1lf\n", sum / 12.0);
	}
	return 0;
}
```

# 744. 数组中的列
```cpp
#include<iostream>
#include<cstdio>
using namespace std;

int main()
{
	int column;
	cin >> column;
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	double sum = 0.0;
	for(int i = 0; i < 12; i++)
	{
		sum = sum + m[i][column];
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else
	{
		printf("%.1lf\n", sum / 12.0);
	}
	return 0;
}
```

# 745. 数组的右上半部分
```cpp
#include<iostream>
using namespace std;

int main()
{
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	int cnt = 0;
	double sum = 0.0;
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			if(i < j)
			{
				sum = sum + m[i][j];
				cnt ++;
			}
		}
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else if(c == 'M')
	{
		printf("%.1lf\n", sum / cnt);		
	}
	return 0;
}
```

# 746. 数组的左下半部分
```cpp
#include<iostream>
#include<cstdio>
using namespace std;

int main()
{
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	double sum = 0.0;
	int column_end = 1;
	for(int i = 1; i < 12; i++)
	{
		for(int j = 0; j < column_end; j++)
		{
			sum = sum + m[i][j];
		}
		column_end ++;
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else
	{
		printf("%.1lf\n", sum / 66);
	}
	return 0;
}
```

# 747. 数组的左上半部分
```cpp
#include<iostream>
using namespace std;

int main()
{
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	int cnt = 0;
	double sum = 0.0;
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12 - i - 1; j++)
		{
			sum = sum + m[i][j];
			cnt ++;
		}
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else if(c == 'M')
	{
		printf("%.1lf\n", sum / cnt);		
	}
	return 0;
}
```

# 748. 数组的右下半部分
```cpp
#include<iostream>
#include<cstdio>
using namespace std;

int main()
{
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	double sum = 0.0;
	int column_start = 1;
	for(int i = 11; i > 0; i--)
	{
		for(int j = column_start; j < 12; j++)
		{
			sum = sum + m[i][j];
		}
		column_start ++;
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else
	{
		printf("%.1lf\n", sum / 66);
	}
	return 0;
}
```


# 749. 数组的上方区域
```cpp
#include<iostream>
using namespace std;

int main()
{
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	int cnt = 0;
	double sum = 0.0;
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12 - i - 1; j++)
		{
			if(i < j)
			{
				sum = sum + m[i][j];
				cnt ++;
			}
		}
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else if(c == 'M')
	{
		printf("%.1lf\n", sum / cnt);		
	}
	return 0;
}
```

# 750. 数组的下方区域
```cpp
#include<iostream>
#include<cstdio>
using namespace std;

int main()
{
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	double sum = 0.0;
	int column_start = 5, column_end = 6;
	for(int i = 7; i < 12; i++)
	{
		int p, q;
		for(p = column_start, q = column_end; p < q; p++, q--)
		{
			sum = sum + m[i][p] + m[i][q];
		}
		column_start --;
		column_end ++;
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else
	{
		printf("%.1lf\n", sum / 30);
	}
	return 0;
}
```

# 751. 数组的左方区域
```cpp
#include<iostream>
using namespace std;

int main()
{
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	int cnt = 0;
	double sum = 0.0;
	for(int j = 0; j < 12; j++)
	{
		for(int i = j + 1; i < 12 - j - 1; i++)
		{
			if(i > j)
			{
				sum = sum + m[i][j];
				cnt ++;
			}
		}
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else if(c == 'M')
	{
		printf("%.1lf\n", sum / cnt);		
	}
	return 0;
}
```

# 752. 数组的右方区域
```cpp
#include<iostream>
#include<cstdio>
using namespace std;

int main()
{
	char c;
	cin >> c;
	double m[12][12];
	for(int i = 0; i < 12; i++)
	{
		for(int j = 0; j < 12; j++)
		{
			cin >> m[i][j];
		}
	}
	
	double sum = 0.0;
	int row_start = 5, row_end = 6;
	for(int j = 7; j < 12; j++)
	{
		int p, q;
		for(p = row_start, q = row_end; p < q; p++, q--)
		{
			sum = sum + m[p][j] + m[q][j];
		}
		row_start --;
		row_end ++;
	}
	
	if(c == 'S')
	{
		printf("%.1lf\n", sum);
	}
	else
	{
		printf("%.1lf\n", sum / 30);
	}
	return 0;
}
```

# 753. 平方矩阵 I
```cpp
#include<iostream>
#include<cstring>
using namespace std;

int main()
{
	int n;
	cin >> n;
	//di和dj表示右、下、左、上
	int di[4] = {0, 1, 0, -1}, dj[4] = {1, 0, -1, 0};
	while(n != 0){
		int hui[n][n];
		memset(hui, 0, sizeof hui);
		//x和y分别表示行坐标和列坐标
		//direction表示前进方向
		//turn表示转向次数
		//value表示要给当前这个圈要赋的值
		int x = 0, y = 0, direction = 0, turn = 0, value = 1;
		//蛇形遍历2维数组
		for(int i = 0; i < n * n; i++)
		{
			hui[x][y] = value;
			int a, b;
			a = x + di[direction];
			b = y + dj[direction];
			
			//此时的判断条件：1.撞墙了；2.已经填好数了。
			if(a < 0 || a >= n || b < 0 || b >= n || hui[a][b] != 0)
			{
				direction = (direction + 1) % 4;
				a = x + di[direction];
				b = y + dj[direction];
				turn ++;
				//此时判断条件表明已经转了一圈了
				if(turn != 0 && turn % 4 == 0)
				{
					value ++;
				}
			}
			x = a;
			y = b;
		}
		
		for(int i = 0; i < n; i++)
		{
			for(int j = 0; j < n; j++)
			{
				if(j == (n - 1))
				{
					cout << hui[i][j] << endl;
				}
				else
				{
					cout << hui[i][j] << " ";
				}
			}
			if(i == n - 1)
			{
				cout << endl;
			}
		}
		cin >> n;
	}
	return 0;
}
```

# 754. 平方矩阵 II
```cpp
#include<iostream>
#include<cstring>
using namespace std;

int main()
{
	int n;
	cin >> n;
	//di和dj表示右、下、左、上
	int di[4] = {0, 1, 0, -1}, dj[4] = {1, 0, -1, 0};
	while(n != 0){
		int hui[n][n];
		memset(hui, 0, sizeof hui);
		//x和y分别表示行坐标和列坐标
		//direction表示前进方向
		//turn表示转向次数
		//value表示要给当前这个圈要赋的值
		int x = 0, y = 0, direction = 0, turn = 0, value = 1;
		//蛇形遍历2维数组
		for(int i = 0; i < n * n; i++)
		{
			hui[x][y] = value;
			int a, b;
			a = x + di[direction];
			b = y + dj[direction];
			
			//此时的判断条件：1.撞墙了；2.已经填好数了。
			if(a < 0 || a >= n || b < 0 || b >= n || hui[a][b] != 0)
			{
				direction = (direction + 1) % 4;
				a = x + di[direction];
				b = y + dj[direction];
				turn ++;
				//此时判断条件表明已经转了一圈了
				if(turn != 0 && turn % 4 == 0)
				{
					value = 0;
				}
			}
			x = a;
			y = b;
			if(turn % 2 == 0)
			{
				value ++;
			}
			else
			{
				value --;
			}
		}
		
		for(int i = 0; i < n; i++)
		{
			for(int j = 0; j < n; j++)
			{
				if(j == (n - 1))
				{
					cout << hui[i][j] << endl;
				}
				else
				{
					cout << hui[i][j] << " ";
				}
			}
			if(i == n - 1)
			{
				cout << endl;
			}
		}
		cin >> n;
	}
	return 0;
}
```

# 755. 平方矩阵 III
```cpp
#include<iostream>
#include<cstring>
#include<cmath>
using namespace std;

int main()
{
	int n;
	cin >> n;
	//di和dj表示右、下、左、上
	int di[4] = {0, 1, 0, -1}, dj[4] = {1, 0, -1, 0};
	while(n != 0){
		int hui[n][n];
		memset(hui, 0, sizeof hui);
		//x和y分别表示行坐标和列坐标
		//direction表示前进方向
		//turn表示转向次数
		//value表示要给当前这个圈要赋的值
		int x = 0, y = 0, direction = 0;
		//蛇形遍历2维数组
		for(int i = 0; i < n * n; i++)
		{
			hui[x][y] = pow(2, (x + y));
			int a, b;
			a = x + di[direction];
			b = y + dj[direction];
			
			//此时的判断条件：1.撞墙了；2.已经填好数了。
			if(a < 0 || a >= n || b < 0 || b >= n || hui[a][b] != 0)
			{
				direction = (direction + 1) % 4;
				a = x + di[direction];
				b = y + dj[direction];
			}
			x = a;
			y = b;
		}
		
		for(int i = 0; i < n; i++)
		{
			for(int j = 0; j < n; j++)
			{
				if(j == (n - 1))
				{
					cout << hui[i][j] << endl;
				}
				else
				{
					cout << hui[i][j] << " ";
				}
			}
			if(i == n - 1)
			{
				cout << endl;
			}
		}
		cin >> n;
	}
	return 0;
}
```

# 756. 蛇形矩阵
```cpp
#include<iostream>
#include<cstring>
using namespace std;

int main()
{
	int n, m;
	cin >> n >> m;
	int snake[n][m];
	int di[4] = {0, 1, 0, -1}, dj[4] = {1, 0, -1, 0};
	memset(snake, 0, sizeof snake);
	int x = 0, y = 0, direction = 0, value = 1;
	for(int i = 0; i < n * m; i++)
	{
		snake[x][y] = value;
		int a, b;
		a = x + di[direction];
		b = y + dj[direction];
			
		if(a < 0 || a >= n || b < 0 || b >= m || snake[a][b] != 0)
		{
			direction = (direction + 1) % 4;
			a = x + di[direction];
			b = y + dj[direction];
		}
		x = a;
		y = b;
		value ++;		
	}
	
	for(int i = 0; i < n; i++)
	{
		for(int j = 0; j < m; j++)
		{
			if(j == (m - 1))
			{
				cout << snake[i][j] << endl;
			}
			else
			{
				cout << snake[i][j] << " ";
			}
		}
	}
	return 0;
}
```

# 760. 字符串长度
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string s;
	getline(cin, s);
	cout << s.size() << endl;
	return 0;
}
```

# 761. 字符串中的数字个数
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string s;
	getline(cin, s);
	int cnt = 0;
	for(int i = 0; i < s.size(); i++)
	{
		if(s[i] >= '0' && s[i] <= '9')
		{
			cnt ++;
		}
	}
	cout << cnt << endl;
	return 0;
}
```

# 762. 字符串匹配
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	double k;
	string a, b;
	cin >> k >> a >> b;
	int cnt = 0;
	for(int i = 0; i < a.size(); i++)
	{
		if(a[i] == b[i])
		{
			cnt ++;
		}
	}
	double rate = cnt / (double)a.size();
	if(rate >= k)
	{
		cout << "yes" << endl;
	}
	else
	{
		cout << "no" << endl;
	}
	return 0;
}
```


# 763. 循环相克令
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	int n;
	cin >> n;
	for(int i = 0; i < n; i++)
	{
		string player1, player2;
		cin >> player1 >> player2;
		if(player1 == player2)
		{
			cout << "Tie" << endl;
		}
		else
		{
			if((player1 == "Hunter" && player2 == "Gun") || (player1 == "Gun" && player2 == "Bear") || (player1 == "Bear" && player2 == "Hunter"))
			{
				cout << "Player1" << endl;
			}
			else
			{
				cout << "Player2" << endl;
			}
		}
	}
	return 0;
}
```

# 764. 输出字符串
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string str;
	getline(cin, str);
	for(int i = 1; i < str.size(); i++)
	{
		cout << (char)(str[i - 1] + str[i]);
	}
	cout << (char)(str[str.size() - 1] + str[0]) << endl;
	return 0;
}
```


# 765. 字符串加空格
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string s;
	getline(cin, s);
	for(int i = 0; i < s.size(); i++)
	{
		if(i == (s.size() - 1))
		{
			cout << s[i] << endl;
		}
		else
		{
			cout << s[i] << " ";
		}
	}
	return 0;
}
```

# 766. 去掉多余的空格
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string str;
	getline(cin, str);
	for(int i = 0; i < str.size(); i++)
	{
		if(str[i] != ' ')
		{
			cout << str[i];
		}
		else
		{
			if(str[i - 1] != ' ')
			{
				cout << str[i];
			}
		}
	}
	return 0;
}
```

# 767. 信息加密
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string str;
	getline(cin, str);
	for(int i = 0; i < str.size(); i++)
	{
		if((str[i] >= 'a' && str[i] <= 'y') || (str[i] >= 'A' && str[i] <= 'Y'))
		{
			str[i] = str[i] + 1;
		}
		else if(str[i] == 'z')
		{
			str[i] = 'a';
		}
		else if(str[i] == 'Z')
		{
			str[i] = 'A';			
		}
	}
	cout << str << endl;
	return 0;
}
```


# 768. 忽略大小写比较字符串大小
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string str1, str2;
	getline(cin, str1);
	getline(cin, str2);
	for(int i = 0; i < str1.size(); i++)
	{
		str1[i] = tolower(str1[i]);
	}
	
	for(int i = 0; i < str2.size(); i++)
	{
		str2[i] = tolower(str2[i]);
	}	
	
	if(str1 == str2)
	{
		cout << "=" << endl;
	}
	else if(str1 > str2)
	{
		cout << ">" << endl;
	}
	else if(str1 < str2)
	{
		cout << "<" << endl;
	}
	return 0;
}
```

# 769. 替换字符
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string s;
	getline(cin, s);
	char c;
	cin >> c;
	for(int i = 0; i < s.size(); i++)
	{
		if(s[i] == c)
		{
			s[i] = '#';
		}
	}
	cout << s << endl;
	return 0;
}
```

# 770. 单词替换
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string str;
	getline(cin, str);
	str = ' ' + str + ' ';
	string dth;
	getline(cin, dth);
	string bth;
	getline(cin, bth);
	int start = 0;
	while(str.find(dth, start) != str.npos)
	{
		int index = str.find(dth, start);
		if(str[index - 1] == ' ' && str[index + dth.size()] == ' ')
		{
			str.replace(index, dth.size(), bth);
		}
		start = index + 1;
	}
	cout << str.substr(1, str.size()) << endl;
	return 0;
}
```

# 771. 字符串中最长的连续出现的字符
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	int n;
	cin >> n;
	while(n)
	{
		string str;
		cin >> str;
		char c = ' ';
		int times = 0;
		for(int i = 0; i < str.size(); i++)
		{
			char ctmp = str[i];
			int ttmp = 0;
			int j;
			for(j = i; j < str.size(); j++)
			{
				if(str[j] == str[i])
				{
					ttmp++;
				}
				else
				{
					break;
				}
			}
			
			if(c == ' ' && times == 0)
			{
				c = ctmp;
				times = ttmp;
			}
			else
			{
				if(ttmp > times)
				{
					c = ctmp;
					times = ttmp;
				}
			}
			
			i = j - 1;
		}
		cout << c << " " << times << endl;		
		n--;
	}

	return 0;
}
```

# 772. 只出现一次的字符
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string str;
	cin >> str;
	int cnt[26] = {0};
	for(int i = 0; i < str.size(); i++)
	{
		cnt[(int)(str[i] - 'a')] ++;
	}
	
	int find = 0;
	for(int i = 0; i < str.size(); i++)
	{
		if(cnt[(int)(str[i] - 'a')] == 1)
		{
			cout << str[i] << endl;
			find = 1;
			break;
		}
	}
	
	if(find == 0)
	{
		cout << "no" << endl;
	}
	
	return 0;
}
```

# 773. 字符串插入
```cpp
#include<iostream>
#include<string>
using namespace std;
int main()
{
	string str, substr;
	while(cin >> str >> substr)
	{
		int index = 0;
		for(int i = 1; i < str.size(); i++)
		{
			if(str[i] > str[index])
			{
				index = i;
			}
		}
		cout << str.substr(0, index + 1) << substr << str.substr(index + 1, str.size()) << endl;
	}
	return 0;
}
```

# 774. 最长单词
```cpp
#include<iostream>
#include<string>
#include<cstring>
using namespace std;
int main()
{
	string str;
	getline(cin, str);
	str = ' ' + str;
	str[str.size() - 1] = ' ';
	int space_index[500];
	memset(space_index, -1, sizeof space_index);
	int flag = 0;
	for(int i = 0; i < str.size(); i++)
	{
		if(str[i] == ' ')
		{
			space_index[flag] = i;
			flag ++;
		}
	}
	
	int length = 0;
	string word;
	for(int i = 0; i < flag - 1; i++)
	{
		int ltmp = space_index[i + 1] - space_index[i] - 1;
		if(ltmp > length)
		{
			int start_index = space_index[i] + 1;	
			word = str.substr(start_index, ltmp);
			length = ltmp;
		}
	}
	cout << word << endl;
	return 0;
}
```

# 775. 倒排单词
```cpp
#include<iostream>
#include<string>
#include<cstring>
using namespace std;
int main()
{
	string str;
	getline(cin, str);
	string word = "";
	string reverse = "";
	for(int i = (str.size() - 1); i >= 0; i--)
	{
		if(str[i] != ' ')
		{
			word = str[i] + word; 
		}
		else
		{
			reverse = reverse + word + ' ';
			word = "";
		}
	}
	reverse = reverse + word;
	cout << reverse << endl;
	return 0;
}
```

# 776. 字符串移位包含问题
```cpp
#include<iostream>
#include<string>
#include<cstring>
using namespace std;
int main()
{
	string str1, str2;
	cin >> str1 >> str2;
	//这里要注意只能是短的是长的字串，所以先做一下预处理
	if(str1.size() < str2.size())
	{
		string tmp;
		tmp = str1;
		str1 = str2;
		str2 = tmp;
	}
	
	//经过处理之后，str1是长的，str2是短的
	string str;
	str = str1;
	int n = str1.size();
	while(n)
	{
		if(n != str1.size())
		{
			char ctmp = str[0];
			int i;
			for(i = 0; i < str.size() - 1; i++)
			{
				str[i] = str[i + 1];
			}
			str[i] = ctmp;
		}
		
		if(str.find(str2) != str.npos)
		{
			break;
		}
		
		n--;
	}
	
	if(n != 0)
	{
		cout << "true" << endl;
	}
	else
	{
		cout << "false" << endl;
	}
	
	return 0;
}
```

# 777. 字符串乘方
```cpp
#include<iostream>
#include<string>
#include<cstring>
using namespace std;
int main()
{
	string str;
	while(cin >> str)
	{
		if(str == ".")
		{
			break;
		}
		else
		{
			int n = 0;
			for(int i = 1; i <= str.size(); i++)
			{
				if(str.size() % i == 0)
				{
					int count = str.size() / i;
					string s = str.substr(0, i);
					string stmp = "";
					for(int j = 0; j < count; j++)
					{
						stmp = stmp + s; 
					}
					if(stmp == str)
					{
						if(count > n)
						{
							n = count;
						}
					}
				}
			}
			cout << n << endl;		
		}
	}
	
	return 0;
}
```

# 778. 字符串最大跨距
```cpp
#include<iostream>
#include<string>
#include<cstring>
using namespace std;
int main()
{
	string input, s, s1, s2;
	cin >> input;
	int index1, index2;
	index1 = input.find(",");
	s = input.substr(0, index1);
	index2 = input.find(",", index1 + 1);
	s1 = input.substr(index1 + 1, index2 - index1 - 1);
	s2 = input.substr(index2 + 1, input.size() - index2 - 1);
	
	int s1_start, s2_start;
	if(s.find(s1) != s.npos)
	{
		s1_start = s.find(s1);
	}
	else
	{
		s1_start = -1;
	}
	
	if(s.find(s2) != s.npos)
	{
		s2_start = s.find(s2);
		int s2_start_tmp = s2_start + 1;
		while(s.find(s2, s2_start_tmp) != s.npos)
		{
			s2_start = s.find(s2, s2_start_tmp);
			s2_start_tmp = s2_start + 1;
		}
	}
	else
	{
		s2_start = -1;
	}
	
	if(s1_start == -1 || s2_start == -1 || s2_start < (s1_start + s1.size()))
	{
		cout << "-1" << endl;
	}
	else
	{
		cout << s2_start - (s1_start + s1.size()) << endl;
	}
	return 0;
}
```

# 779. 最长公共字符串后缀
```cpp
#include<iostream>
#include<string>
#include<cstring>
using namespace std;
int main()
{
	int n;
	while(cin >> n)
	{
		if(n == 0)
		{
			break;
		}
		else
		{
			string str[n];
			for(int i = 0; i < n; i++)
			{
				cin >> str[i];
			}
			int length[n], max_length = 0;
			
			for(int i = 0; i < n; i++)
			{
				length[i] = str[i].size();
				if(length[i] > max_length)
				{
					max_length = length[i];
				}
			}
			
			for(int i = 0; i < n; i++)
			{
				if(length[i] < max_length)
				{
					for(int j = 0; j < max_length - length[i]; j++)
					{
						str[i] = "*" + str[i];
					}
				}
			}
			
			int cnt = 0;
			for(int j = str[0].size() - 1; j >= 0; j--)
			{
				int flag = 1;
				char ctmp = str[0][j];
				for(int i = 1; i < n; i++)
				{
					if(str[i][j] != ctmp)
					{
						flag = 0;
						break;
					}
				}
				
				if(flag == 1)
				{
					cnt++;
				}
				else
				{
					break;
				}
			}
			
			if(cnt == 0)
			{
				cout << endl;
			}
			else
			{
				cout << str[0].substr(max_length - cnt, cnt) << endl;
			}
		}
	}
	return 0;
}
```

# 804. n的阶乘
```c
#include<iostream>
using namespace std;

int fact(int n)
{
	int jiecheng = 1;
	for(int i = 1; i <= n; i++)
	{
		jiecheng = jiecheng * i;
	}
	return jiecheng;
}

int main()
{
	int n;
	cin >> n;
	int result;
	result = fact(n);
	cout << result << endl;
	return 0;
}
```

# 805. x和y的最大值
```c
#include<iostream>
using namespace std;

int max(int x, int y)
{
	if(x >= y)
	{
		return x;
	}
	else
	{
		return y;
	}
}

int main()
{
	int x, y;
	cin >> x >> y;
	int result;
	result = max(x, y);
	cout << result << endl;
	return 0;
}
```

# 808. 最大公约数
```c
#include<iostream>
using namespace std;

int gcd(int a, int b)
{
	//两个值中较大的值用a存，较小的用b存
	if(a < b)
	{
		int temp1;
		temp1 = a;
		a = b;
		b = temp1;
	}
	
	//辗转相除法（欧几里德法）
	int temp2;
	while(b != 0)
	{
		temp2 = a % b;
		a = b;
		b = temp2;
	}
	return a;
}

int main()
{
	int a, b;
	cin >> a >> b;
	int result;
	result = gcd(a, b);
	cout << result << endl;
	return 0;
}
```

# 810. 绝对值
```c
#include<iostream>
using namespace std;
int abs(int x);
int main()
{
	int x;
	cin >> x;
	cout << abs(x) << endl;
	return 0;
} 

int abs(int x)
{
	if(x >= 0)
	{
		return x;
	}
	else
	{
		return -1 * x;
	}
}
```

# 811. 交换数值
```c
#include<iostream>
using namespace std;

void swap(int &x, int &y)
{
	int temp;
	if(x != y)
	{
		temp = x;
		x = y;
		y = temp;
	}
}

int main()
{
	int x, y;
	cin >> x >> y;
	swap(x, y);
	cout << x << " " << y << endl;
	return 0;
}
```

# 812. 打印数字
```c
#include<iostream>
using namespace std;
void print(int a[], int size);
int main()
{
	int n, size;
	cin >> n >> size;
	int a[n];
	for(int i = 0; i < n; i++)
	{
		cin >> a[i];
	}
	print(a, size);
	return 0;
} 

void print(int a[], int size)
{
	for(int i = 0; i < size; i++)
	{
		if(i == size - 1)
		{
			cout << a[i] << endl;
		}
		else
		{
			cout << a[i] << " ";
		}
	}
}
```

# 813. 打印矩阵
```c
#include<iostream>
using namespace std;
//定义数组的行数和列数
const int m = 100;
const int n = 100;
//定义数组
int shuzu[m][n];

//这里注意参数中的二维数组不能写成int a[][]，当多维数组作为函数参数的时候，需要指定除了第一个维度的其它维度的大小
void print2D(int a[m][n], int row, int col);
int main()
{
	int row, col;
	cin >> row >> col;
	for(int i = 0; i < row; i++)
	{
		for(int j = 0; j < col; j++)
		{
			cin >> shuzu[i][j];
		}
	}
	print2D(shuzu, row, col);
	return 0;
} 

void print2D(int a[m][n], int row, int col)
{
	for(int i = 0; i < row; i++)
	{
		for(int j = 0; j < col; j++)
		{
			if(j == col - 1)
			{
				cout << a[i][j] << endl;
			}
			else
			{
				cout << a[i][j] << " ";
			}
		}
	}
}
```

# 819. 递归求阶乘
```c
#include<iostream>
using namespace std;
int jiecheng(int n);
int main()
{
	int n;
	cin >> n;
	cout << jiecheng(n) << endl;
	return 0;
} 

int jiecheng(int n)
{
	if(n == 1)
	{
		return 1;
	}
	else
	{
		return n * jiecheng(n - 1);
	}
}
```

# 820. 递归求斐波那契数列
```c
#include<iostream>
using namespace std;
int fbnq(int n);
int main()
{
	int n;
	cin >> n;
	cout << fbnq(n) << endl;
	return 0;
} 

int fbnq(int n)
{
	if(n == 1 || n == 2)
	{
		return 1;
	}
	else
	{
		return fbnq(n - 1) + fbnq(n - 2);
	}
}
```

