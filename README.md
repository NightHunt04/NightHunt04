#include<stdio.h>
#include<stdlib.h>

struct nd{
	int data;
	struct nd *link;
};

struct nd* sort(struct nd *head){
	struct nd *current=head, *index=NULL;
	int temp;
	while(current!=NULL){
		index=current->link;
		while(index!=NULL){
			if(current->data > index->data){
				temp=current->data;
				current->data=index->data;
				index->data=temp;
			}
			index=index->link;
		}
		current=current->link;
	}
	return head;
}

int main()
{
	
	return 0;
}
