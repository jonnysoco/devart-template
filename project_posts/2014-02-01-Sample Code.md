## Sample Code

Below is a sample piece of code, writtten in <a href="https://www.dartlang.org/" target="_blank">Google Dart</a> to process twitter's json search results.

```
processBack(String jsonString) {
  List<String> jsonResult = JSON.decode(jsonString);
    for (int i = 0; i < jsonResult.length; i++) {
    var listObj = jsonResult[i];
    feelingsUl.children.add(new LIElement()..text = listObj['text']);
    }
  querySelector('.feelingsUl li').classes.toggle('loaded', true);
  runMonitor();
}
```
