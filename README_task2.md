Step 1: Create a new Flutter project
Run the following command to create a new Flutter project:

```bash
flutter create multi_screen_app
```

## Step 2: Update main.dart
Replace the content of main.dart with the following code:

```dart
import 'package:flutter/material.dart';
import 'screens/tab_screen.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Multi-Screen App',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: TabScreen(),
    );
  }
}
```

## Step 3: Create TabScreen widget
Create a new file tab_screen.dart and define the TabScreen widget:

```dart
import 'package:flutter/material.dart';
import 'screens/screen1.dart';
import 'screens/screen2.dart';
import 'screens/screen3.dart';

class TabScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return DefaultTabController(
      length: 3,
      child: Scaffold(
        appBar: AppBar(
          title: Text('Tabbed Navigation'),
          bottom: TabBar(
            tabs: [
              Tab(icon: Icon(Icons.home), text: 'Screen 1'),
              Tab(icon: Icon(Icons.search), text: 'Screen 2'),
              Tab(icon: Icon(Icons.person), text: 'Screen 3'),
            ],
          ),
        ),
        body: TabBarView(
          children: [
            Screen1(),
            Screen2(),
            Screen3(),
          ],
        ),
      ),
    );
  }
}
```

## Step 4: Create Screen1, Screen2, and Screen3 widgets
Create three separate files screen1.dart, screen2.dart, and screen3.dart with the respective widget content for each screen. For example:

screen1.dart:

```dart
import 'package:flutter/material.dart';

class Screen1 extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Center(
      child: Text('Screen 1 Content'),
    );
  }
}
```

### screen2.dart:

```dart
import 'package:flutter/material.dart';

class Screen2 extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Center(
      child: Text('Screen 2 Content'),
    );
  }
}

```

### screen3.dart:

```dart
import 'package:flutter/material.dart';

class Screen3 extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Center(
      child: Text('Screen 3 Content'),
    );
  }
}
```

### Step 5: Run the application
Execute the following command to run your Flutter app:
```
flutter run
```
