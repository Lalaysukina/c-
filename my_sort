# c-
//比较函数
void swap(char* a, char* b, int si)
{
	int i = 0;
	for (i = 0; i < si; i++)  //因为char*只能访问一个字节，要换si(元素大小)次才能把一个元素换完
	{
		char tmp = *a;
		*a = *b;
		*b = tmp;
		a++;
		b++;
	}
}
//qsort函数（此函数为从小到大排列，若要从大到小排列，需改变判断条件，将返回值>0改成<0）
void my_qsort(void* arr,int sz,int si,int (*int_cmp)(void* a,void* b))  //qsort函数需要 排序数组的首元素地址、要排序元素的数量、单个元素的大小、判断函数（需自己实现）
{
	int i = 0;
	for (i = 0; i < sz - 1; i++) //冒泡排序的趟数
	{
		int j = 0;
		for (j = 0; j < sz - 1 - i; j++)  //一个元素需要比较的次数
		{
			if (int_cmp((char*)arr + si*j, (char*)arr + si*(j + 1)) > 0)  //判断函数  该元素若大于相邻元素则返回>0的整数，小于相邻函数则返回<0的整数，相等返回0
			{
				swap((char*)arr + si*j, (char*)arr + si*(j + 1), si);  //交换函数
			}
		}
	}
}
