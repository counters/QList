# QList
Linked list library for Arduino

Purpose of this library is to enable programers to create lists of things

First, we create simple list object example for ints:
``` C++
  QList<int> list;
```

Then we can add items in list:
``` C++
  list.push_front(item); // Push item at the front of the list
  list.push_back(item); // Push item at the back of the list
```

Items on the list can be removed:
``` C++
  list.pop_front(); // Remove item at the front of the list
  list.pop_back(); // Remove item at the back of the list
  /*
    Remove item at given position
    WARNING !
    Note:
      - index starts with 0 not 1 so interval is [0,n)
      - always check if index is in valid range before you try to clear item
  */
  list.clear(index);
```
Items on the list can accessed:
``` C++
  int val1 = list.front(); // Get item at the front of the list
  int val2 = list.back(); // Get item at the back of the list
  /*
    Get item at given position
    WARNING !
    Note:
      - index starts with 0 not 1 so interval is [0,n)
      - always check if index is in valid range before you try to clear item
  */
  int val3 = list.at(index);
  int val3 = list.get(index);
```
Size of list can be accessed with:
``` C++
  int list_size = list.size();
  int same_list_size = list.legth();
```

You can also search for items in list:
``` C++
  int pos = list.indexOf(item);
  if(pos < 0)
    Serial.println("Item not found");
```
Note: If item is not found function returns -1
