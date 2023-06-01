/*----------------------------------

背景色をつけ、高さと幅を設定しよう！

①全体の背景色を追加
②プロフィール欄に幅と高さをつける

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
          // ★：①全体の背景色を追加
          backgroundColor: Colors.yellow.shade50,
          appBar: AppBar(title: const Text('自己紹介')),
          body: Center(
            child: Container(
              // ★：②プロフィール欄に幅と高さをつける
              width: 300,
              height: 500,
              child: Column(
                children: [
                  Row(
                    children: [Text('名前'), Text('なかじま')],
                  ),
                  Row(
                    children: [Text('住み'), Text('神奈川')],
                  ),
                  Row(
                    children: [Text('誕生日'), Text('01/12')],
                  ),
                  Row(
                    children: [Text('趣味'), Text('音楽')],
                  ),
                  Row(
                    children: [Text('ひとこと'), Text('どんなアプリ作ろうか')],
                  )
                ],
              ),
            ),
          )),
    );
  }
}
