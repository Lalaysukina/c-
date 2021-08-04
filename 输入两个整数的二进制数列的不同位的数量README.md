# c-int main()
{
	int i = 0;
	int count = 0;
	int m = 0;
	int n = 0;
	scanf("%d %d", &m, &n);
	for (i = 0; i < 32; i++)
	{
		if (((m >> i) & 1) != ((n >> i) & 1))
		{
			count++;
		}
	}
	printf("%d\n", count);
	return 0;
}
