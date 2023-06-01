/*----------------------------------

要素を縦に並べよう！

①Columnを追加（Ctrl + . を活用しよう！）
②Childrenに配列を作り、中にTextを並べる

----------------------------------*/
```Dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Profile',
      theme: ThemeData(primarySwatch: Colors.blue),
      home: Scaffold(
          appBar: AppBar(title: const Text('自己紹介')),
          body: Center(
            child: Container(
              // ★：①Columnを追加（Ctrl + . を活用しよう！）
              child: Column(
                // ★：②Childrenに配列を作り、中にTextを並べる
                children: [
                  Text('中島'),
                  Text('神奈川'),
                  Text('01/12'),
                  Text('音楽'),
                  Text('どんなアプリを作ろうか'),
                ],
              ),
            ),
          )),
    );
  }
}
