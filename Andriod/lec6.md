#  creating a ListView

in xml file 
-

![image](https://github.com/user-attachments/assets/0bd6f496-dc5c-4d9c-b82d-2ee9ee399b6f)

![image](https://github.com/user-attachments/assets/00e28cde-9249-44bf-a587-e72f294cfcf2)

![image](https://github.com/user-attachments/assets/a4c73241-1e72-4fae-bae5-a7f3b8b7a571)

```
ListView listView = findViewById(R.id.listView);
String[] days = {"Saturday", "Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday"};

```
 create a string array, which will be the data source for the ListView.
```
ArrayAdapter<String> adapter = new ArrayAdapter<>(getApplicationContext(), android.R.layout.simple_list_item_1, days);

listView.setAdapter(adapter);
```
ArrayAdapter is used to convert the array of strings (values) into ListView items.
the adapter links the data source to the ListView, using a simple built-in layout (android.R.layout.simple_list_item_1).
ArrayAdapter is a simple adapter used for mapping each string in values to the layout specified by simple_list_item_1.
listView.setAdapter(adapter) connects the adapter to the ListView.

![image](https://github.com/user-attachments/assets/37971525-c4a4-4f43-a9e3-87c3e6224207)
![image](https://github.com/user-attachments/assets/038ceb2c-67fc-44f4-a658-fcb08b607acc)

Define What Happens When a User Interacts with a Row:
-
```
listView.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> adapterView, View row, int position, long id) {
                Toast.makeText(MainActivity.this, adapter.getItem(position), Toast.LENGTH_SHORT).show();
            }
        });

```

![image](https://github.com/user-attachments/assets/02884e87-cf0d-45af-bc07-dac85af335d6)



Steps to Display a Complex ListView with Custom Adapter
-
In a complex ListView, each row may contain multiple views (e.g., TextView, ImageView, Button, etc.). To achieve this, you will create a custom adapter that binds data to a custom row layout.

It's prohibited for images placed in the drawable folder to have a name that is a number.












