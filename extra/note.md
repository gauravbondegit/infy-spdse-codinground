<img width="410" height="381" alt="image" src="https://github.com/user-attachments/assets/c5b98b7b-db9f-4bea-8809-93920536962c" />
<img width="341" height="191" alt="image" src="https://github.com/user-attachments/assets/0809d439-7823-48da-9ac2-0176bbc68654" />

# Trie

```java
class TrieNode {
    TrieNode[] ch = new TrieNode[26];
    boolean end;
}

TrieNode root = new TrieNode();

void insert(String s) {
    TrieNode p = root;
    for (char c : s.toCharArray()) {
        int i = c - 'a';
        if (p.ch[i] == null) {
            p.ch[i] = new TrieNode();
        }
        p = p.ch[i];
    }
    p.end = true;
}

boolean search(String s) {
    TrieNode p = root;
    for (char c : s.toCharArray()) {
        int i = c - 'a';
        if (p.ch[i] == null) return false;
        p = p.ch[i];
    }
    return p.end;
}

boolean startsWith(String prefix) {
    TrieNode p = root;
    for (char c : prefix.toCharArray()) {
        int i = c - 'a';
        if (p.ch[i] == null) return false;
        p = p.ch[i];
    }
    return true;
}
```
