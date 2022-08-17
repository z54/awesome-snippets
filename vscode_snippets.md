---
id: 1t73ap2vnszk7bk0l88tund
title: Vscode_snippets
desc: ''
updated: 1660666548383
created: 1660666548383
---
# vscode_snippets

## usage

[Snippets in Visual Studio Code](https://code.visualstudio.com/docs/editor/userdefinedsnippets)

type a snippet prefix (trigger text), and press Tab to insert a snippet.

## Markdown

%userprofile%\AppData\Roaming\Code\User\snippets\markdown.json

### Codeblock

```json
    // Codeblock
    "codeblock": {
        "prefix": "code",
        "body": [
            "```$1",
            "```",
        ],
        "description": "codeblock"
    },
    "mermaid codeblock": {
        "prefix": "mermaid",
        "body": [
            "```mermaid",
            "graph $1",
            "```",
        ],
        "description": "mermaid codeblock"
    },
    "bash codeblock": {
        "prefix": "bash, sh",
        "body": [
            "```bash",
            "$1",
            "```",
        ],
        "description": "bash codeblock"
    },
    "json codeblock": {
        "prefix": "json",
        "body": [
            "```json",
            "$1",
            "```",
        ],
        "description": "json codeblock"
    },
    "cmd codeblock": {
        "prefix": "cmd, bat",
        "body": [
            "```cmd",
            "$1",
            "```",
        ],
        "description": "cmd codeblock"
    },
```

### tinymind

```json
    // mindmap

    // extension need, qiqiworld.vscode-markdown-tinymind
    
    "tinymind codeblock": {
        "prefix": "tinymind, mind, mindmap",
        "body": [
            "```tinymind",
            "根节点",
            "\t一级节点$1",
            "```",
        ],
        "description": "tinymind codeblock"
    },
```

### dot

```json
    // dot

    // [Node Shapes | Graphviz](https://graphviz.org/doc/info/shapes.html)
    // box, ellipse, circle, house, pentagon, default: ellipse

    // [Layout Engines | Graphviz](https://graphviz.org/docs/layouts/)
    // dot, fdp, default: dot

    // [rankdir | Graphviz](https://graphviz.org/docs/attrs/rankdir/)
    // TB, LR, default: TB
    
    "graph codeblock": {
        "prefix": "graph, dot, graphviz",
        "body": [
            "```graphviz",
            "graph g {", // 无向图
                "\trankdir=\"TB\" // TB, LR, default: TB", 
                "\tnode [shape=box]; // box, ellipse, circle, house, pentagon, default: ellipse", 
                "\ta -- b [label = \"eg\"]$1",
                "}",
            "```",
        ],
        "description": "dot graph codeblock"
    },
    "digraph codeblock": {
        "prefix": "digraph, dot, graphviz",
        "body": [
            "```graphviz",
            "digraph g {", // 有向图
                "\tnode [shape=box]; // box, ellipse, circle, house, pentagon, default: ellipse", 
                "\ta1 -> b1 [label = \"eg\"]$1",
                "}",
            "```",
        ],
        "description": "dot digraph codeblock"
    },
    "neato codeblock": {
        "prefix": "neato, dot, graphviz",
        "body": [
            "```graphviz",
            "graph g {",
                "\tlayout=neato // dot, fdp, default: dot", 
                "\tnode [shape=box]; // box, ellipse, circle, house, pentagon, default: ellipse", 
                "\ta1 -- b1 [label = \"eg\"]$1",
                "}",
            "```",
        ],
        "description": "dot neato codeblock"
    },
    "subgraph codeblock": {
        "prefix": "subgraph, dot, graphviz",
        "body": [
            "subgraph cluster_sub {",
                "\ta1 -- b1 [label = \"eg\"]$1",
                "}",
        ],
        "description": "dot subgraph codeblock"
    },
```

## c

%userprofile%\AppData\Roaming\Code\User\snippets\markdown.json

```json
	"c main": {
        "prefix": "c main",
        "body": [
            "int main(String[] args){",
                "\tprintf(\"Hello,World!\");",
                "\treturn 0;",
            "}",
        ],
        "description": "c main"
    },
```
