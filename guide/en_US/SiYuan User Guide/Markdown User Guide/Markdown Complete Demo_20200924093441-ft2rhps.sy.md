## Tutorial
{: id="20200924094024-qtk2ywa"}

This is an example of how to correctly use **Markdown** typesetting. It is necessary to learn this to make your article better and clearer.
{: id="20200924094024-jt3xw1o"}

> Quoted text: Markdown is a text formatting syntax inspired
> {: id="20200924094024-6zs53jq"}
{: id="20200924094024-yed7vhb"}

## Grammar guide
{: id="20200924094024-p7y8ufo"}

### Content block reference
{: id="20200924094024-lboyuty"}

`((20200924101312-jj4e0v3 "Content block reference"))`
{: id="20200924212626-ua83wse"}

((20200924101312-jj4e0v3 "Content block reference"))
{: id="20200924094024-hvlcrvt"}

### Content block embedding
{: id="20200924094024-s0oyhvp"}

`!((20200924101312-385dey5 "Content block embedding"))​`
{: id="20200924094024-kwo2mbm"}

!((20200924101312-385dey5 "Content block embedding"))
{: id="20200924212640-bvx8qbj"}

### General content
{: id="20200924094024-ac7p9zy"}

This content shows some layout formats in the content, such as:
{: id="20200924094024-7pllcxl"}

-**Bold**-`**Bold**`
-*Tilt*-`*Tilt*`
-~~Strikethrough~~-`~~Strikethrough~~`
-`Code tag`-`` `Code tag` ``
-[Hyperlink](https://ld246.com)-`[Hyperlink](https://ld246.com)`
-[username@gmail.com](mailto:username@gmail.com)-`[username@gmail.com](mailto:username@gmail.com)`
{: id="20200924094024-q16ihi5"}

### Emoji Emoji
{: id="20200924094024-yqqmjy8"}

Support most standard emoticons, you can use the input method to input directly or manually input the character format. Trigger auto completion by entering `:`.
{: id="20200924094024-kpl5gfx"}

#### Some emoticons examples
{: id="20200924094024-jf7b8mb"}

:smile: :laughing: :dizzy_face: :sob: :cold_sweat: :sweat_smile: :cry: :triumph: :heart_eyes: :relieved::+1: :-1: :100: :clap: :bell: :gift: :question: :bomb: :heart: :coffee: :cyclone: :bow: :kiss: :pray: :anger:
{: id="20200924094024-6yl5wi3"}

### Heading
{: id="20200925103734-dkxfu63"}

Use one `#` for the first-level heading, two `##` for the second-level heading, and so on, up to six-level headings are supported.
{: id="20200924094024-bc6k656"}

> NOTE: Don't forget # needs to have a space after it!
> {: id="20200924094024-8zdnn2x"}
{: id="20200924094024-m7yc3db"}

### Pictures
{: id="20200924094024-t9yqr2j"}

```
![alt text](http://image-path.png)
![alt text](http://image-path.png "Image Title Value")
```
{: id="20200924094024-6httwnw"}

Support direct copy and paste.
{: id="20200924094024-s5mg6rq"}

### Code block
{: id="20200924094024-j18xcet"}

#### Ordinary
{: id="20200924094024-xo5xekv"}

```
*emphasize* **strong**
_emphasize_ __strong__
var a = 1
```
{: id="20200924094024-bu430x1"}

#### Syntax highlighting support
{: id="20200924094024-ubgm4kt"}

If the language name is followed by ```, it can have the effect of syntax highlighting, for example:
{: id="20200924094024-ii9hstv"}

##### Demonstrate Go code highlighting
{: id="20200924094024-4un6enc"}

```go
package main

import "fmt"

func main() {
fmt.Println("Hello, World")
}
```
{: id="20200924094024-9h4qacz"}

##### Demo Java highlighting
{: id="20200924094024-a1tht5s"}

```java
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello World!");
    }

}
```
{: id="20200924094024-nvmczcu"}

> Tip: Language names support the following: `ruby`, `python`, `js`, `html`, `erb`, `css`, `coffee`, `bash`, `json`, `yml`, ` xml` ...
> {: id="20200924094024-4k11kbh"}
{: id="20200924094024-fywn6dv"}

### Ordered, unordered, task list
{: id="20200924094024-cmd3uci"}

#### Unordered List
{: id="20200924094024-0h7f098"}

-Java
{: id="20200924094024-nsg5prm"}

-Spring
-IoC
-AOP
-Go
{: id="20200924094024-sabyoz8"}

-gofmt
-Wide
-Node.js
{: id="20200924094024-ocryeki"}

-Koa
-Express
{: id="20200924094024-0kw4d2i"}

#### Ordered List
{: id="20200924094024-81xq38o"}

1. Node.js
   {: id="20200924094024-qznwlou"}

   1. Express
   2. Koa
   3. Sails
   {: id="20200924094024-o1skv8j"}
2. Go
   {: id="20200924094024-eipn0tl"}

   1. gofmt
   2. Wide
   {: id="20200924094024-z4r69k9"}
3. Java
   {: id="20200924094024-4fvsra1"}

   1. Latke
   2. IDEA
   {: id="20200924094024-gaeaz15"}
{: id="20200924094024-ejvrtvu"}

#### task list
{: id="20200924094024-f96q2vh"}

-[X] Publish Sym
-[X] Release Solo
-[] Book a dentist
{: id="20200924094024-esueclg"}

### Form
{: id="20200924094024-xbuqupm"}

If you need to display data or something, you can choose to use a table.
{: id="20200924094024-go9q56f"}

| header 1 | header 2 |
| - | - |
| cell 1 | cell 2 |
| cell 3 | cell 4 |
| cell 5 | cell 6 |
{: id="20200924094024-j1e0bvy"}

### Paragraph
{: id="20200924094024-l6cykrd"}

Blank lines can divide the content into sections for easy reading. (This is the first paragraph)
{: id="20200924094024-9qti343"}

Using blank lines is very important in Markdown typesetting. (This is the second paragraph)
{: id="20200924094024-hzs5ijg"}

### Link reference
{: id="20200924094024-pfkti37"}

[Link text][Link label]
{: id="20200924093949-2wdmv8h"}

```
[Link text][link label]

[Link label]: https://b3log.org
```
{: id="20200924093949-f6ueq1j"}

### Mathematical formula
{: id="20200924094024-hincz1r"}

Multi-line formula block:
{: id="20200924094024-l9nabvm"}

$$
\frac{1}{
  \Bigl(\sqrt{\phi \sqrt{5}}-\phi\Bigr) e^{
  \frac25 \pi}} = 1+\frac{e^{-2\pi}} {1+\frac{e^{-4\pi}} {
    1+\frac{e^{-6\pi}}
    {1+\frac{e^{-8\pi}}{1+\cdots}}
  }
}
$$
{: id="20200924094024-4oz0cby"}

In-line formula:
{: id="20200924094024-fimshra"}

The formula $a^2 + b^2 = \color{red}c^2$ is inline.
{: id="20200924093443-2e46q4r"}

### Mind Map
{: id="20200924093558-waooqpg"}

```mindmap
- Tutorial
- Grammar guidance
  - General content
  - Mention users
  - Emoji
    - Some emoji examples
  - Heading-Heading 3
    - Heading 4
      - Heading 5
        - Heading 6
  - Picture
  - Code block
    - Normal
    - Syntax highlighting support
      - Demonstrate Go code highlighting
      - Demo Java highlighting
  - Ordered, disordered, task list
    - Unordered list
    - Ordered list
    - task list
  - Form
  - Hide details
  - Paragraph
  - Link reference
  - Mathematical formula
  - Mind Map
  - Flow chart
  - Timing diagram
  - Gantt chart
  - Chart
  - Staff
  - Graphviz
  - Multimedia
  - Footnote
  - Shortcuts
```
{: id="20200924094024-dgq81gr"}

### Flow chart
{: id="20200924094024-7vldo7v"}

```mermaid
graph TB
    c1-->a2
    subgraph one
    a1-->a2
    end
    subgraph two
    b1-->b2
    end
    subgraph three
    c1-->c2
    end
```
{: id="20200924094024-gtseufm"}

### Timing diagram
{: id="20200924094024-1tkuvf2"}

```mermaid
sequenceDiagram
    Alice->>John: Hello John, how are you?
    loop Every minute
        John-->>Alice: Great!
    end
```
{: id="20200924094024-z8sjbh6"}

### Gantt chart
{: id="20200924094024-4zjkp1f"}

```mermaid
gantt
    title A Gantt Diagram
    dateFormat YYYY-MM-DD
    section Section
    A task :a1, 2019-01-01, 30d
    Another task :after a1, 20d
    section Another
    Task in sec :2019-01-12, 12d
    another task: 24d
```
{: id="20200924094024-98yhbjl"}

### Chart
{: id="20200924094024-ikqifr8"}

```echarts
{
  "title": { "text": "Latest 30 days" },
  "tooltip": { "trigger": "axis", "axisPointer": { "lineStyle": { "width": 0 } } },
  "legend": { "data": ["Articles", "Users", "Replies"] },
  "xAxis": [{
      "type": "category",
      "boundaryGap": false,
      "data": ["2019-05-08","2019-05-09","2019-05-10","2019-05-11","2019-05-12","2019-05-13","2019-05-14","2019-05-15","2019-05-16","2019-05-17","2019-05-18","2019-05-19","2019-05-20","2019-05-21","2019-05-22","2019-05-23","2019-05-24","2019-05-25","2019-05-26","2019-05-27","2019-05-28","2019-05-29","2019-05-30","2019-05-31","2019-06-01","2019-06-02","2019-06-03","2019-06-04","2019-06-05","2019-06-06","2019-06-07"],
      "axisTick": { "show": false },
      "axisLine": { "show": false }
  }],
  "yAxis": [{ "type": "value", "axisTick": { "show": false }, "axisLine": { "show": false }, "splitLine": { "lineStyle": { "color": "rgba(0, 0, 0, .38)", "type": "dashed" } } }],
  "series": [
    {
      "name": "Articles", "type": "line", "smooth": true, "itemStyle": { "color": "#d23f31" }, "areaStyle": { "normal": {} }, "z": 3,
      "data": ["18","14","22","9","7","18","10","12","13","16","6","9","15","15","12","15","8","14","9","10","29","22","14","22","9","10","15","9","9","15","0"]
    },
    {
      "name": "Users", "type": "line", "smooth": true, "itemStyle": { "color": "#f1e05a" }, "areaStyle": { "normal": {} }, "z": 2,
      "data": ["31","33","30","23","16","29","23","37","41","29","16","13","39","23","38","136","89","35","22","50","57","47","36","59","14","23","46","44","51","43","0"]
    },
    {
      "name": "Replies", "type": "line", "smooth": true, "itemStyle": { "color": "#4285f4" }, "areaStyle": { "normal": {} }, "z": 1,
      "data": ["35","42","73","15","43","58","55","35","46","87","36","15","44","76","130","73","50","20","21","54","48","73","60","89","26","27","70","63","55","37","0"]
    }
  ]
}
```
{: id="20200924093622-1bi5x7q"}

### Staff
{: id="20200924093627-ri25pre"}

```abc
X: 24
T: Clouds Thicken
C: Paul Rosen
S: Copyright 2005, Paul Rosen
M: 6/8
L: 1/8
Q: 3/8=116
R: Creepy Jig
K: Em
|:"Em"EEE E2G|"C7"_B2A G2F|"Em"EEE E2G|\
"C7"_B2A "B7"=B3|"Em"EEE E2G|
"C7"_B2A G2F|"Em"GFE "D (Bm7)"F2D|\
1"Em"E3-E3:|2"Em"E3-E2B|:"Em"e2e gfe|
"G"g2ab3|"Em"gfeg2e|"D"fedB2A|"Em"e2e gfe|\
"G"g2ab3|"Em"gfe"D"f2d|"Em"e3-e3:|
```
{: id="20200924094024-kp3w88n"}

### Graphviz
{: id="20200924094024-a29tkxn"}

```graphviz
digraph finite_state_machine {
     rankdir=LR;
     size="8,5"
     node [shape = doublecircle]; S;
     node [shape = point ]; qi

     node [shape = circle];
     qi -> S;
     S -> q1 [label = "a" ];
     S -> S [label = "a" ];
     q1 -> S [label = "a" ];
     q1 -> q2 [label = "ddb" ];
     q2 -> q1 [label = "b" ];
     q2 -> q2 [label = "b" ];
}
```
{: id="20200924094024-qsyx5t1"}

## Shortcuts
{: id="20200924094024-2cnw1gq"}

Our editor supports many shortcut keys, please refer to ((20200924100950-9op5xi1 "Editor and shortcuts")) for details.
{: id="20200924094024-hrypk1t"}
