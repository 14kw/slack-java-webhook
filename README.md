# typetalk-java-api
Java Client to Typetalk incoming webhook. 

## Usage
```java
// Using TypetalkMessage
new Typetalk(endpointUrl)
    .push(new TypetalkMessage("This repository is ").link("https://github.com/14kw/typetalk-java-webhook", "Typetalk-Java-Client"));

// Using TypetalkAttachment
new Typetalk(endpointUrl)
    .push(new TypetalkAttachment("https://avatars2.githubusercontent.com/u/1132256?s=460&v=4", "14kw avatar"));

// Using TypetalkMessage And TypetalkAttachment
new Typetalk(endpointUrl)
    .push(
        new TypetalkMessage("This repository is ").link("https://github.com/14kw/typetalk-java-webhook", "Typetalk-Java-Client"),
        new TypetalkAttachment("https://avatars2.githubusercontent.com/u/1132256?s=460&v=4", "14kw avatar")
    );

```

## Notes
With `TypetalkMessage` you can create rich text as specified in https://developer.nulab-inc.com/ja/docs/typetalk/formatting/. Example usage

Available methods on `TypetalkMessage`
- `text`
- `link`
- `code`
- `preformatted`
- `quote`

## License

http://www.apache.org/licenses/LICENSE-2.0
