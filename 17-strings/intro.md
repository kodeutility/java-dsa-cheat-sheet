# String

### Java String methods
|Description|Method|
|---|---|
||str.charAt()|
||str.contains()|
||str1.equals(str2)|
||str1.equalsIgnoreCase(str2)|
||str.indexOf()|
||str.lastIndexOf()|
||str.isEmpty()|
||str.length()|
||str.split()|
||str.toUpperCase()|
||str.toLowerCase()|
||str.toCharArray()|
||str.trim()|
||str.substring()|
||str.subSequence()|
||str.startsWith()|
||str.endsWith()|
||str.replace()|
||str.replaceFirst()|
||str.replaceAll()|

- To use for loop over string use str.toCharArray()
```java
for(char c : s.toCharArray()){
            mp.put(c, mp.getOrDefault(c,0) + 1);
        }
```
# String Builder
- StringBuilder is mutable in java
