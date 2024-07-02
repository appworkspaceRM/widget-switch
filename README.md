# flutter_application_23

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

# Switch Widget

merupakan wigdet yang dapat perpindah kondisi saat ada event tap. ini bisa digukana untuk pengkondisian tema tau semacamnya karna value dari switch meruapakan boolean dan bisa kita ganti true dan false.

![Capture](https://github.com/appworkspaceRM/widget-switch/assets/135511281/94b4a7e3-0abf-441b-9487-0e54755c5e4d)


```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      home: HomePage(),
    );
  }
}

class HomePage extends StatefulWidget {
  const HomePage({super.key});

  @override
  State<HomePage> createState() => _HomePageState();
}

class _HomePageState extends State<HomePage> {
  bool isSwitched = false;
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Switch'),
      ),
      body: Center(
        child: Column(
          children: [
            Switch(
              activeColor: Colors.green,
              activeTrackColor: Colors.red,
              inactiveTrackColor: Colors.blue,
              inactiveThumbColor: Colors.amber,
              value: isSwitched,
              onChanged: (value) {
                setState(() {
                  isSwitched = value;
                });
              },
            ),
            Text(isSwitched ? 'SWITCH ON' : 'SWITCH OFF')
          ],
        ),
      ),
    );
  }
}

```

![code-snapshot](https://github.com/appworkspaceRM/widget-switch/assets/135511281/0d12bd29-d3b1-42b8-8982-8cdbdf9f1c7d)
