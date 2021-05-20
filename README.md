# Reproducion steps

- Generate C# sources for both files `Message1` and `Message2`:
```quicktype --src Message1.json --src-lang schema --lang csharp --features attributes-only --namespace MyNamespace --out Message1.cs```
```quicktype --src Message2.json --src-lang schema --lang csharp --features attributes-only --namespace MyNamespace --out Message2.cs```

- Expected: code should compile.

- Actual result: code won't compile because `Message1` and `Message2` define the same `MyEnumType`.
