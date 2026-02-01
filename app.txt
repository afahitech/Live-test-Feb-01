import 'package:flutter/material.dart';

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: ContactListScreen(),
    );
  }
}

class ContactListScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(


        backgroundColor: Colors.blue[200],
        title: Text('Contact List'),
        centerTitle: true,
      ),
      body: Padding(
        padding: EdgeInsets.all(18.0),
        child: Column(
          children: [
            // Name Field
            TextFormField(
              decoration: InputDecoration(
                labelText: 'Name',
                border: OutlineInputBorder(),
              ),
            ),
            SizedBox(height: 16),

            // Mobile Number Field
            TextFormField(
              decoration: InputDecoration(
                labelText: 'Mobile Number',
                border: OutlineInputBorder(),
              ),
              keyboardType: TextInputType.phone,
            ),
            SizedBox(height: 16),

            // Add Button
            ElevatedButton(

              onPressed: () {},
              style: ElevatedButton.styleFrom(
                backgroundColor: Colors.blue[200],
                minimumSize: Size(double.infinity, 50),
              ),
              child: Text('Add Contact'),
            ),
            SizedBox(height: 24),

            // Contact List
            Expanded(
              child: ListView(
                children: [
                  ListTile(
                    leading: Icon(Icons.person),
                    title: Text('Jawad', style: TextStyle(color: Colors.red),),
                    subtitle: Text('01745-777777'),
                    trailing: Icon(Icons.phone, color: Colors.blue,),
                  ),
                  ListTile(
                    leading: Icon(Icons.person),
                    title: Text('Ferdous', style: TextStyle(color: Colors.red),),
                    subtitle: Text('01745-777777'),
                    trailing: Icon(Icons.phone,color: Colors.blue),
                  ),
                  ListTile(
                    leading: Icon(Icons.person),
                    title: Text('Hasan', style: TextStyle(color: Colors.red),),
                    subtitle: Text('01745-777777'),
                    trailing: Icon(Icons.phone,color: Colors.blue),
                  ),
                  ListTile(
                    leading: Icon(Icons.person),
                    title: Text('Hasan',style: TextStyle(color: Colors.red),),
                    subtitle: Text('01745-777777'),
                    trailing: Icon(Icons.phone,color: Colors.blue),
                  ),
                  ListTile(
                    leading: Icon(Icons.person),
                    title: Text('Hasan', style: TextStyle(color: Colors.red),),
                    subtitle: Text('01745-777777'),
                    trailing: Icon(Icons.phone,color: Colors.blue),
                  ),
                  ListTile(
                    leading: Icon(Icons.person),
                    title: Text('Ferdous', style: TextStyle(color: Colors.red),),
                    subtitle: Text('01745-777777'),
                    trailing: Icon(Icons.phone,color: Colors.blue),
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
