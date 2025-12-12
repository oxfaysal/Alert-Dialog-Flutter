# Alert Dialog Flutter



### Dialog - Function
```
ShowDialog(context){
    return showDialog(
        context: context,
        builder: (BuildContext context){
          return Expanded(
              child: AlertDialog(
                title: Text("Love !"),
                content: Text("This is a love of paradise"),
                backgroundColor: Colors.cyanAccent,
                actions: [
                  OutlinedButton(onPressed: (){Navigator.pop(context);}, child: Text("No")),
                  OutlinedButton(onPressed: (){
                    MySnacbar("This Love Accept", context);
                    Navigator.pop(context);
                  }, child: Text("Yes")),
                ],
              )
          );
        },
    );
}

```





### Dialog - Function (With Image)
```
ShowDialog(context){
    return showDialog(
        context: context,
        builder: (BuildContext context){
          return Expanded(
              child: AlertDialog(
                title: Text("Love !"),
                content: Column(children: [
                  Text("This is a love of paradise"),
                  Image.network("https://avatars.githubusercontent.com/u/248434219",
                    height: 250,
                    fit: BoxFit.cover,
                    errorBuilder: (context, error, stackTrace) {
                      return Text(
                        'Failed to load image',
                        style: TextStyle(color: Colors.red),
                      );
                    },
                  )
                ],),
                backgroundColor: Colors.cyanAccent,
                actions: [
                  OutlinedButton(onPressed: (){Navigator.pop(context);}, child: Text("No")),
                  OutlinedButton(onPressed: (){
                    MySnacbar("This Love Accept", context);
                    Navigator.pop(context);
                  }, child: Text("Yes")),
                ],
              )
          );
        },
    );
}
```


###### © All Right reserved by **Faysal**

