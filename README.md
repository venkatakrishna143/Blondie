# Blondie
#include <stdio.h>
#include<math.h>

int main(void) {
	// your code goes here
	int tc;
	scanf("%d",&tc);
	while(tc--)
	{
	    long int n;
	    scanf("%ld",&n);
	    long int a[n],ps[n];
	    for(int i=0;i<n;i++)
	    {
	        scanf("%ld",&a[i]);
	        if(i==0)
	            ps[i]=a[i];
	        else
	        {
	            if(a[i]==-1)
	                a[i]=floor(ps[i-1]/i);
	            ps[i]=ps[i-1]+a[i];
	        }
	    }
	    for(int i=0;i<n;i++)
	       printf("%d ",a[i]);
	   printf("\n");
	}
	
	return 0;
}

