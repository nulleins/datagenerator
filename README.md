# matchspliterator
A `Spliterator` capable traversing and partitioning elements from a regular expression `Matcher`, applying a `Consumer` to act 
upon the matching text

Example
-------
``` java
    final Matcher matcher = Pattern.compile("\\d+").matcher("12: this text contains 3 numbers (123)");
    final MatchSpliterator matchit = new MatchSpliterator(matcher, m -> m.group());
    final Stream<String> results = StreamSupport.stream(matchit, false);
    System.out.println(results.collect(Collectors.joining("+")));
```    
