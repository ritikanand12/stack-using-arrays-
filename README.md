Stack Implementation Using Array in C

This project demonstrates the implementation of a Stack data structure using an array in C.

📖 Description

The program:

Defines a stack structure using an array

Implements basic stack operations:

✅ Push

✅ Pop

✅ Peek

✅ isFull

✅ isEmpty

Demonstrates stack operations in the main() function

The stack follows the LIFO (Last In, First Out) principle.

🧠 Stack Operations
🔹 1. Push

Adds an element to the top of the stack.

Checks for overflow (stack full).

Increments top and inserts value.

⏱ Time Complexity: O(1)

🔹 2. Pop

Removes and returns the top element.

Checks for underflow (stack empty).

Returns the top element and decrements top.

⏱ Time Complexity: O(1)

🔹 3. Peek

Returns the top element without removing it.

⏱ Time Complexity: O(1)

🖥️ Program Code
#include <stdio.h>
#include <stdlib.h>

#define MAX 5

// Stack structure
struct Stack {
    int arr[MAX];
    int top;
};

// Function to initialize the stack
void initStack(struct Stack* stack) {
    stack->top = -1;
}

// Function to check if the stack is full
int isFull(struct Stack* stack) {
    return stack->top == MAX - 1;
}

// Function to check if the stack is empty
int isEmpty(struct Stack* stack) {
    return stack->top == -1;
}

// Function to push an element onto the stack
void push(struct Stack* stack, int value) {
    if (isFull(stack)) {
        printf("Stack is full!\n");
    } else {
        stack->arr[++stack->top] = value;
        printf("%d pushed to stack\n", value);
    }
}

// Function to pop an element from the stack
int pop(struct Stack* stack) {
    if (isEmpty(stack)) {
        printf("Stack is empty!\n");
        return -1;
    } else {
        return stack->arr[stack->top--];
    }
}

// Function to peek the top element of the stack
int peek(struct Stack* stack) {
    if (isEmpty(stack)) {
        printf("Stack is empty!\n");
        return -1;
    } else {
        return stack->arr[stack->top];
    }
}

// Main function
int main() {
    struct Stack stack;
    initStack(&stack);

    push(&stack, 10);
    push(&stack, 20);
    push(&stack, 30);

    printf("Top element is %d\n", peek(&stack));

    printf("%d popped from stack\n", pop(&stack));
    printf("%d popped from stack\n", pop(&stack));

    printf("Top element is %d\n", peek(&stack));

    return 0;
}
▶️ How to Run
Step 1: Compile the program
gcc stack.c -o stack
Step 2: Run the program
./stack
📝 Sample Output
10 pushed to stack
20 pushed to stack
30 pushed to stack
Top element is 30
30 popped from stack
20 popped from stack
Top element is 10
⚠️ Stack Limit

Maximum size is defined as #define MAX 5

You can change MAX to increase stack capacity.

🎯 Features

Simple and modular implementation

Uses structure for stack representation

Handles overflow and underflow conditions

Beginner-friendly code

📚 Author

Ritik Chauhan

If you want, I can also create:

🔹 Stack using linked list

🔹 Menu-driven stack program

🔹 Infix to postfix using stack

🔹 Full Data Structures project README 🚀
