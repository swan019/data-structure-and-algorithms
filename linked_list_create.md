//swapnil ingale
#include <iostream>
using namespace std;

class node{
    public:
    int data;
    node* next;
};

void print_linked_list(node * head)
{
    cout << "print linked list " << endl;
    node* ptr = head;
    while(ptr != NULL)
    {
        cout << ptr->data << " ";
        ptr = ptr->next;
    }
}
int main()
{
    int n;
    cout << "Enter total number of element in linked list : ";
    cin >> n;

    node * head, * last, * temp;
    head = new node;
    int i = 1;
    int k;
    cout << "Enter " << i << " element : ";
    cin >> k;
    head->data = k;
    head->next = NULL;

    last = head;
    i++;
    while(i<=n)
    {
        cout << "Enter " << i << " element : ";
        cin >> k;
        temp = new node;
        temp->data = k;
        temp->next = NULL;
        last->next = temp;

        last = temp;

        i++;
    }

    print_linked_list(head);

    cout << endl;
    cout << temp->data << " " << last->data << endl;
    cout << temp->next << " " << last->next << endl;

    return 0;

}
