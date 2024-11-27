
#include <iostream>
using namespace std;
class Node{
  
  public:
  Node*next;
  Node*prev;
  int data;
  Node(int value){
      prev=nullptr;
      next=nullptr;
      data=value;
  }
  Node*head=nullptr;
};
void push(Node** head_ref,int new_data){
    Node*new_node=new Node(new_data);
    new_node->next=(*head_ref);
    new_node->data=new_data;
    new_node->prev=nullptr;
    if((*head_ref)!=nullptr){
        (*head_ref)->prev=new_node;
    }
    (*head_ref)=new_node;
}
void display(Node*head){
    Node*temp=head;
    while(temp!=nullptr){
        cout<<temp->data<<" ";
        temp=temp->next;
        
    }
}

void addLast(Node** head_ref, int data) {
    Node* new_node = new Node(data);
    new_node->next = nullptr;
    
    // If the list is empty, new node becomes the head
    if (*head_ref == nullptr) {
        new_node->prev = nullptr;
        *head_ref = new_node;
        return;
    }

    Node* last = *head_ref;
    while (last->next != nullptr) {
        last = last->next;
    }

    last->next = new_node;
    new_node->prev = last;
}
int search(Node*head,int data){
    Node*current=head;
    while(current != nullptr){
        if(current-> data== data){
            cout<< "Value "<<data<<" is found in the list."<<endl;
            return data;
    }
    current= current->next;
}

cout<< "Value is not found."<<endl;
return 0;


}

int main()
{
    Node*head=nullptr;
    cout<<"Doubly linked list that is adding from last:"<<endl;
    
    addLast(&head,9);
    addLast(&head,19);
    addLast(&head,95);
    display(head);
    cout<<endl;
    cout<<"Doubly linked list that is adding from beginning:"<<endl;
    push(&head,10);
    push(&head,20);
    push(&head,30);
    display(head);
    cout<<endl;
    search(head,40);
    search(head,10);

    return 0;
}
