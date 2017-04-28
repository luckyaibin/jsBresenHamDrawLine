"# jsBresenHamDrawLine" 
#include<iostream>
#include<stdio.h>

int ZigZag(int n)
{
	int v = (n << 1) ^ (n >> 31);
	return v;
}

int UnZigZag(int n)
{
	int v = ((unsigned int)n >> 1) ^ (-(n & 1));
	return v;
}
int main() {

	printf("%s", "hello");
	for (int i=-10;i<11;i++)
	{
		int zigzag = ZigZag(i);
		int unzigzag = UnZigZag(zigzag);
		printf("%d -> %d  ,%d \n",i, zigzag, unzigzag);
	}

	//int i = (int)(0xFFFFFFFF);
	int i = (int)(0x80000000);
	int zigzag = ZigZag(i);
	int unzigzag = UnZigZag(zigzag);

	return 0;
}
