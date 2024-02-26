# Gi-i-b-t-ph-ng-tr-nh-b-c-nh-t
Lập trình giải bất phương trình ax+b>0 theo yêu cầu: Viết 1 hàm nhập các hệ số a, b; một hàm giải bất phương trình. Hàm main sử dụng các hàm đã viết và có thể chạy nhiều lần giải các bất phương trình khác nhau.
#include <conio.h>
#include <stdio.h>
#include <iostream.h>

void nhap(float &, float &);
void giaibpt(float, float);
void main()

{
	float a, b;
	char c;
	do {
		clrscr();
		nhap(a, b);
		giaibpt(a, b);
		fflush(stdin);
		cout << "\nTiep tuc ? (c/k):";
		cin >> c;
	} while ((c == 'c') || (c == 'C'));
}

void nhap(float &a, float &b)
{
	cout << "Nhap cac he so a, b :";
	cin >> a >> b;
}

void giaibpt(float a, float b)
{
	if (a > 0) cout << "Nghiem x>" << -b / a;
	else if (a < 0) cout << "Nghiem x<" << -b / a;
	else if (b > 0) cout << "Vo so nghiem";
	else cout << "Vo nghiem";
}
