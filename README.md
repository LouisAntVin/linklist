# linklist

## Implementing a linklist with INSERT and DISPLAY operations
```
#include<stdio.h>
#include<stdlib.h>

void main()
{
	struct node
	{
		int data;
		struct node *next;
	};
	
	struct node *head=NULL,*pos=NULL,*tail=NULL;
	
	int ch, entry;
	
	while(1)
	{
		printf("\n1:Insert\n2:Display\n3:Exit\n");
		printf("Enter your choice :");
		scanf("%d",&ch);
		
		switch(ch)
		{
			case 1:
			{
				printf("Enter data");
				scanf("%d",&entry);
				if(head==NULL)
				{
					head=(struct node*)malloc(sizeof(struct node));
					head->data=entry;
					pos=head;
					tail=head;
				}
				else
				{
					tail->next=(struct node*)malloc(sizeof(struct node));
					tail=tail->next;
					tail->data=entry;
				}
				break;
			}
			
			case 2:
			{
				pos=head;
				printf("\nElements are: ");
				while(pos!=NULL)
				{
					printf("\t%d",pos->data);
					pos=pos->next;
				}
				break;
			}
			
			case 3:
			{
				printf("\nExiting...");
				exit(0);
			}
		}
	}
}

```
## Counting the number of elements in a linklist
```
#include<stdio.h>
#include<stdlib.h>

void main()
{
	struct node
	{
		int data;
		struct node *next;
	};
	
	struct node *head=NULL,*pos=NULL,*tail=NULL;
	
	int ch, entry,c;
	
	while(1)
	{
		printf("\n1:Insert\n2:Display\n3:Count\n4:Exit\n");
		printf("Enter your choice :");
		scanf("%d",&ch);
		
		switch(ch)
		{
			case 1:
			{
				printf("Enter data");
				scanf("%d",&entry);
				if(head==NULL)
				{
					head=(struct node*)malloc(sizeof(struct node));
					head->data=entry;
					pos=head;
					tail=head;
				}
				else
				{
					tail->next=(struct node*)malloc(sizeof(struct node));
					tail=tail->next;
					tail->data=entry;
				}
				break;
			}
			
			case 2:
			{
				pos=head;
				printf("\nElements are: ");
				while(pos!=NULL)
				{
					printf("\t%d",pos->data);
					pos=pos->next;
				}
				break;
			}
			
			case 3:
			{
				pos=head;
				c=0;
				printf("\nNumber of elements are: ");
				while(pos!=NULL)
				{
					c++;
					pos=pos->next;
				}
				printf("%d",c);
				break;
			}
			case 4:
			{
				printf("\nExiting...");
				exit(0);
			}
		}
	}
}
```

## Searching an element in a linklist
```
#include<stdio.h>
#include<stdlib.h>

void main()
{
	struct node
	{
		int data;
		struct node *next;
	};
	
	struct node *head=NULL,*pos=NULL,*tail=NULL;
	
	int ch, entry,c=0,k,t,temp;
	
	while(1)
	{
		printf("\n\n1:Insert\n2:Display\n3:Count\n4:Search\n5:Exit\n");
		printf("Enter your choice :");
		scanf("%d",&ch);
		
		switch(ch)
		{
			case 1:
			{
				printf("Enter data");
				scanf("%d",&entry);
				if(head==NULL)
				{
					head=(struct node*)malloc(sizeof(struct node));
					head->data=entry;
					pos=head;
					tail=head;
				}
				else
				{
					tail->next=(struct node*)malloc(sizeof(struct node));
					tail=tail->next;
					tail->data=entry;
				}
				break;
			}
			
			case 2:
			{
				pos=head;
				printf("\nElements are: ");
				while(pos!=NULL)
				{
					printf("\t%d",pos->data);
					pos=pos->next;
				}
				break;
			}
			
			case 3:
			{	c=0;
				pos=head;
				printf("\nNumber of elements are: ");
				while(pos!=NULL)
				{
					c++;
					pos=pos->next;
				}
				printf("%d",c);
				break;
			}
			
			case 4:
			{
				c=0;
				t=1;
				pos=head;
				printf("Enter data to search: ");
				scanf("%d",&k);
				while(pos!=NULL)
				{	
					c++;
					temp=pos->data;
					pos=pos->next;
					if(temp==k)
					{
						t=0;
						printf("Element is at position %d",c);
						break;
					}
				}
				if(t)
					printf("Element not found");
				break;
			}
			
			case 5:
			{
				printf("\nExiting...");
				exit(0);
			}
		}
	}
}
```
