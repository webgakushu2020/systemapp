/*----------------------------------

変更を加えられる箇所と、そうでない箇所に分けよう！その1

①MyHomePageという新しいクラスを作ろう
②さらに_MyHomePageStateという新しいクラスを作ろう
③homeの背景色backgroundColorだけコピペしよう

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
          backgroundColor: Colors.yellow.shade50,
          appBar: AppBar(title: const Text('自己紹介')),
          body: Center(
            child: Container(
              width: 300,
              height: 500,
              decoration: BoxDecoration(
                  color: Colors.white,
                  border: Border.all(color: Colors.brown, width: 2),
                  borderRadius: BorderRadius.circular(20)),
              padding: EdgeInsets.all(10),
              child: ListView(
                children: [
                  Image.asset("images/sakura.jpg"),
                  Padding(
                    padding: EdgeInsets.only(bottom: 5),
                    child: Row(
                      children: [Text('名前'), SizedBox(width: 5), Text('とも')],
                    ),
                  ),
                  Padding(
                    padding: EdgeInsets.only(bottom: 5),
                    child: Row(
                      children: [Text('住み'), SizedBox(width: 5), Text('神奈川')],
                    ),
                  ),
                  Padding(
                    padding: EdgeInsets.only(bottom: 5),
                    child: Row(
                      children: [
                        Text('誕生日'),
                        SizedBox(width: 5),
                        Text('01/12')
                      ],
                    ),
                  ),
                  Padding(
                    padding: EdgeInsets.only(bottom: 5),
                    child: Row(
                      children: [Text('趣味'), SizedBox(width: 5), Text('音楽')],
                    ),
                  ),
                  Row(
                    children: [
                      Text('ひとこと'),
                      SizedBox(width: 5),
                      Flexible(
                          child: Text(
                              'どんなアプリ作ろうか。そういえばメッセージって長くなりがちだよね。そんな時も安心！Flexibleで囲ってあげれば、自動的にこんな感じで折り返してくれるよ。ちなみに改行をしたい場合は\nをつけるとできるよ！\n\n2個連続ももちろんオッケー！'))
                    ],
                  ),
                  SizedBox(height: 10),
                  Row(
                    children: [
                      TextButton(
                        onPressed: () {},
                        child: Text('文字'),
                      ),
                      SizedBox(width: 5),
                      OutlinedButton(
                        onPressed: () {},
                        child: Text('文字'),
                      ),
                      SizedBox(width: 5),
                      ElevatedButton(
                        onPressed: () {},
                        child: Text('文字'),
                      ),
                    ],
                  )
                ],
              ),
            ),
          )),
    );
  }
}

// ★：①MyHomePageという新しいクラスを作ろう（コピペでOK）

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key, required this.title});
  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

// ★：②さらに_MyHomePageStateという新しいクラスを作ろう

class _MyHomePageState extends State<MyHomePage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      // ★：③homeの背景色backgroundColorだけコピペしよう
      backgroundColor: Colors.yellow.shade50,
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(),
    );
  }
}
