class Stack_LL {
private:
	// topPtr points to the top element of the stack (to array)
    bool empty = true;
    int* stack;
    int total = 0;

public:

	Stack_LL();
	~Stack_LL();

	bool isEmpty() const;
	void push(int newItem);
	void pop();
	int peek() const;
};

Stack_LL::Stack_LL() {
    stack = new int[1];    //new arry with capacity made
}

Stack_LL::~Stack_LL() {
	delete[] stack; //empty data pointer
	stack = nullptr;
}

bool Stack_LL::isEmpty() const {
    return empty;
}

void Stack_LL::push(int newItem) 
{    
    empty = false;
    
    // 1. make new array large enough for everything
	total++;
	int* newArray = new int[total];

	//2. copy new data.
    newArray[0] = newItem;
    
    //3. copy old data
	for (unsigned int i = 0; i < (total - 1); i++)
	{
		newArray[i + 1] = stack[i];
	}
    
	//3. replace old arry
	delete[] stack;
	stack = newArray;
}

void Stack_LL::pop() {
    
    //1. check if it will empty the array
    total--;
    if(total < 1)
    {
        total = 0;
        empty = true;
        return;
    }
    
    //2. If the array isn't empty, make new shorter array
    int* newArray = new int[total];
    
    //3. Copy data
    for(int i = 0; i < (total); i++)
    {
        newArray[i] = stack[i + 1];
    }
    
    //4. replace old arry
	delete[] stack;
	stack = newArray;
}

int Stack_LL::peek() const {
    
	return stack[0];
}
