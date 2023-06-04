---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# page transition
transition: slide-left
# use UnoCSS
css: unocss
---

# A Comprehensive Study on SolOSphere: An Advanced Tool Suite for Solidity Contract Optimization

SolOSphere the ultimate solution for solidty contracts

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---


# Introduction
The advent of Solidity Smart Contracts

- Solidity as the primary language for Ethereum Smart Contracts.
- The rise of smart contracts and their potential to revolutionize contractual agreements.

<img src="/res/ethereum.jpg" alt="Ethereum" width="500" height="500"/>


---
transition: slide-up
---

# Introduction (cont.)
Problem Statement

- The inefficiencies and complexities of current smart contracts due to inefficient gas usage.
- The gap between the potential of smart contracts and their real-world performance.


---
transition: slide-up
---

# Introduction (cont.)
The Solution

- Introduction to SolOSphere, the comprehensive suite designed for contract optimization.
- Overview of SolOSphere components: SolO, SolOLab, SMARTS, and SMARTS-GPT.
- How SolOSphere addresses the issue of inefficient gas usage in smart contracts.


---
transition: slide-up
---

# Background
Solidity Smart Contracts

- **Solidity**: A statically-typed, contract-oriented programming language widely used for developing Ethereum Smart Contracts.
- **Smart Contracts**: Autonomous, self-executing contracts with the terms of the agreement directly written into code. They exist across a distributed, decentralized blockchain network.
- **Role of Solidity in Smart Contracts**: Solidity provides the necessary constructs to build complex contracts on the Ethereum network, fostering a wide range of decentralized applications (DApps).

```mermaid
graph LR
  Solidity -->|Develops| Ethereum_Smart_Contracts
  Ethereum_Smart_Contracts -->|Exists In| Blockchain
  Ethereum_Smart_Contracts -->|Allows| Decentralized_Applications
```

---
transition: slide-up
---

# Background (cont.)
Gas in Ethereum Network

- **Gas**: An internal pricing unit for running transactions or smart contracts on Ethereum.
- **Purpose of Gas**: Used to allocate resources of the Ethereum virtual machine (EVM), ensuring that contracts run efficiently and securely.
- **Gas and Contract Execution**: Each operation in the execution of a contract consumes a certain amount of gas, with more complex computations requiring more gas.


```mermaid
graph LR
  Transactions -->|Requires| Gas
  Gas -->|Allocates Resources of| EVM
  Gas -->|Determines Efficiency of| Smart_Contract_Execution
```

---
transition: slide-up
---

# Background (cont.)
Miners and the Ethereum Network

- **Miners**: Individuals or entities that validate new transactions and record them on the global ledger (blockchain).
- **Role of Miners**: Miners play a crucial role in maintaining the integrity of the Ethereum network. They validate and execute smart contract computations.
- **Gas and Miners**: Miners are compensated for their computational work in 'gas fees', which are paid by the users initiating the smart contract.

```mermaid
graph LR
  Miners -->|Validates and Records| Transactions
  Miners -->|Maintains Integrity of| Ethereum_Network
  Users -->|Pays| Gas_Fees
  Gas_Fees -->|Compensates| Miners
```
---
transition: slide-up
---

# Background (cont.)
Parsing and Deploying Smart Contracts

- **Parsing**: The process of analyzing a string of symbols in a programming language. In the context of Solidity contracts, parsing refers to reading and interpreting the contract's code.
- **Deploying**: The process of taking a contract written in Solidity and placing it onto the Ethereum blockchain, where it is executed within the EVM.

```mermaid
graph LR
  Solidity_Contracts -- Parsing --> Interpreted_Contracts
  Interpreted_Contracts -- Optimizing --> Optimized_Contracts
  Optimized_Contracts -- Deploying --> Ethereum_Blockchain
```


---
transition: slide-up
---

# Methodology
Overview

- Process begins with the utilization of SMARTS to scrape GitHub for contract source codes.
- These source codes are parsed and unparsed using SolO to verify its functionality.
- Generation of new contracts using SMARTS-GPT and text-DaVinci-003 model.
- Deployment of generated contracts and comparison of gas usage between optimized and unoptimized versions using SolOLab.
- Creation and mutation of custom contracts for further testing and verification of SolO.

```mermaid
graph LR
  A[Scrape GitHub Using SMARTS] --> B[Parse and Unparse Using SolO]
  B --> C[Generate Contracts Using SMARTS-GPT]
  C --> D[Deploy and Compare Gas Using SolOLab]
  D --> E[Create and Mutate Custom Contracts]
```

---
transition: slide-up
---

# Methodology (cont.)
SMARTS and GitHub

- SMARTS retrieves smart contract source codes from GitHub.
- 612 files were tested to verify the functionality of SolO's parser and unparser.
- Challenges faced: Out of 612 files, 417 did not function due to unparser errors.


```mermaid
graph LR
  A[SMARTS] -- Scrapes --> B[GitHub Source Codes]
  B -- Tests --> C[SolO Parser and Unparser]
  C -- Faces Challenges --> D[417 Files with Unparser Errors]
```

---
transition: slide-up
---

# Methodology (cont.)
SMARTS-GPT and Contract Generation

- SMARTS-GPT, with the text-DaVinci-003 model, was used to generate 192 new contracts.
- Minor fixes were required in some contracts due to inaccuracies in the GPT model.
- These contracts were used to verify the deployment and comparison of gas consumption in SolOLab.

```mermaid
graph LR
  A[SMARTS-GPT with text-DaVinci-003 Model] --> B[Generation of 192 New Contracts]
  B -- Requires Fixes --> C[Contracts with Inaccuracies]
  C -- Used for Verification --> D[Deployment and Gas Comparison in SolOLab]
```

---
transition: slide-up
---

# Methodology (cont.)
SolOLab and Contract Deployment

- Contracts were divided into two folders - optimized and unoptimized.
- Python Brownie was used to deploy the contracts and compare the gas usage.
- Results: Slight optimization in gas, but all contracts were successfully deployed.


```mermaid
graph LR
  A[Contracts Divided into Optimized and Unoptimized] --> B[Deployment Using Python Brownie]
  B -- Compares Gas Usage --> C[Results: Slight Gas Optimization]
  B -- Confirms Successful Deployment --> C
```

---
transition: slide-up
---
# Methodology (cont.)
Custom Contracts

- Five custom contracts were created for testing.
- Using GPT, these contracts were mutated into 50 unique versions.
- The mutated contracts were deployed and their gas was compared, demonstrating successful optimization, particularly for loops.


```mermaid
graph TB
  A[Creation of Five Custom Contracts] --> B[Mutation into 50 Unique Versions using GPT]
  B -- Deployed and Gas Compared --> C[Successful Optimization, Particularly for Loops]
```

---
transition: slide-up
---

# SoloSphere Components

List of all the components


- 🥼**SolOLab** - This component focuses on the experiments
- 📱 **SMARTS** - This component focuses on scraping smart contracts
- ☢️ **SolO** - The main core optimizer

```mermaid
graph LR
  A[Raw Solidity Contracts] -->|Input| B(SolOSphere)
  B -->|Parsing| C{Solidity Parser}
  C -->|Abstract Syntax Tree AST| D[SolO Optimizer]
  D -->|Optimized AST| E{Unparser}
  E -->|Optimized Source Code| F[Optimized Solidity Contracts]
  B -->|SMARTS| G[Contract Retrieval from GitHub]
  B -->|SMARTS-GPT| H[Contract Generation]
  H --> C
  G --> C
  B -->|SolOLab| I[Deployment & Gas Comparison]
  F --> I
  click B "https://github.com/SolOSphere"
  style B fill:#f9d,stroke:#333,stroke-width:2px
  style C fill:#fd9,stroke:#333,stroke-width:2px
  style D fill:#9df,stroke:#333,stroke-width:2px
  style E fill:#9fd,stroke:#333,stroke-width:2px
  style F fill:#df9,stroke:#333,stroke-width:2px
  style G fill:#f9d,stroke:#333,stroke-width:2px
  style H fill:#9fd,stroke:#333,stroke-width:2px
  style I fill:#9fd,stroke:#333,stroke-width:2px
```

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
transition: slide-up
layout: two-cols
---

# SolO
Parser


```solidity
contract SimpleContract {
  uint x;
  uint total = 100;
  
  function setX(uint _x) public {
    x = _x;
  }
}
```


::right::

```mermaid
graph TB
  Root --> Contract[Contract: SimpleContract]
  Contract --> StateVariableDeclaration1[StateVariableDeclaration: x]
  StateVariableDeclaration1 --> VariableDeclaration1[VariableDeclaration: uint x]
  Contract --> StateVariableDeclaration2[StateVariableDeclaration: total]
  StateVariableDeclaration2 --> VariableDeclaration2[VariableDeclaration: uint total]
  VariableDeclaration2 --> NumberLiteral[NumberLiteral: 100]
  Contract --> FunctionDefinition[FunctionDefinition: setX]
  FunctionDefinition --> Parameter[Parameter: _x]
  Parameter --> VariableDeclaration3[VariableDeclaration: uint _x]
  FunctionDefinition --> ExpressionStatement[ExpressionStatement: x = _x]
  ExpressionStatement --> Identifier1[Identifier: x]
  ExpressionStatement --> Identifier2[Identifier: _x]

```


---
transition: slide-up
layout: two-cols
---

# SolO Patterns
**SolO** - The main core optimizer

- Packing
  - Struct Packing ✅ 
  - Variable Packing ✅ 
  - Boolean Packing ⛔️
- Types
  - Uint* vs Uint256 ⛔️
  - Bytes vs Strings ⛔️
  - Fixed Size ✅
  - Default Value ✅ 
- Data Location
  - Call Data vs Memory ✅ 
  - Freeing Storage ⛔️

::right::

- Function Visibility
  - Internal vs External  ✅
  - Constant and Immutable  ✅
- Operation Reduction
  - Reducing Expression  ✅
  - Short Circuiting ⛔️
  - Write Values   ✅
  - Single Line Swap ✅
- Function Reduction
  - Limit Number of Functions ⛔️
  - Limit Modifiers ⛔️
- Loop Combination
  - Prohibit The Use of Nested Loops ⛔️
  - Simplify Multiple Loops ⛔️
  - Repetitive Arithmetic Operations in Loop ✅

---
transition: slide-up
layout: two-cols
---

# SolO Patterns (cont.)
**SolO** - The main core optimizer

- Caching
  - Cache Storage Variable  ✅
  - Caching Member Variable  ✅
  - Cache Array Length ✅
  - Loop Increment ✅ 
- Mapping 
  - Mapping vs Array ⛔️


---
transition: slide-up
---

# SolO Patterns (cont.)
High level Optimizations Overview

```mermaid
graph LR
  Start[Start: Solidity Contract Source Code] --> Parser[Load Contract into Solidity Parser]
  Parser --> Parse[Parse: Break Contract into Syntax Tree]
  Parse --> Traverse1{Traverse Syntax Tree}
  Traverse1 --> PatternMatch1{Pattern Match?}
  PatternMatch1 --> |Yes| ApplyPattern1[Apply SolO Pattern]
  ApplyPattern1 --> Traverse2{Traverse Syntax Tree}
  Traverse2 --> PatternMatch2{Pattern Match?}
  PatternMatch2 --> |Yes| ApplyPattern2[Apply Another SolO Pattern]
  ApplyPattern2 --> Traverse3{Traverse Syntax Tree}
  Traverse3 --> PatternMatch3{Pattern Match?}
  PatternMatch3 --> |Yes| ApplyPattern3[Apply Another SolO Pattern]
  PatternMatch1 --> |No| End[End: Optimized Solidity Contract Source Code]
  PatternMatch2 --> |No| End
  PatternMatch3 --> |No| End

```

```mermaid
graph LR;
    A[Raw Solidity Contract]
    B[Parser]
    C[Abstract Syntax Tree AST]
    D[Optimizer]
    E[Optimized AST]
    F[Unparser]
    G[Optimized Solidity Contract]
    A-->B;
    B-->C;
    C-->D;
    D-->E;
    E-->F;
    F-->G;
    class A phase1
    class B phase2
    class C phase3
    class D phase4
    class E phase5
    class F phase6
    class G phase7
    classDef phase1 fill:#f9d,stroke:#333,stroke-width:2px;
    classDef phase2 fill:#fd9,stroke:#333,stroke-width:2px;
    classDef phase3 fill:#9df,stroke:#333,stroke-width:2px;
    classDef phase4 fill:#9fd,stroke:#333,stroke-width:2px;
    classDef phase5 fill:#df9,stroke:#333,stroke-width:2px;
    classDef phase6 fill:#f9d,stroke:#333,stroke-width:2px;
    classDef phase7 fill:#9fd,stroke:#333,stroke-width:2px;

```

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Code

Use code snippets and get the highlighting directly![^1]

```ts {all|2|1-6|9|all}
interface User {
  id: number
  firstName: string
  lastName: string
  role: string
}

function updateUser(id: number, update: User) {
  const user = getUser(id)
  const newUser = { ...user, ...update }
  saveUser(id, newUser)
}
```

<arrow v-click="3" x1="400" y1="420" x2="230" y2="330" color="#564" width="3" arrowSize="1" />

[^1]: [Learn More](https://sli.dev/guide/syntax.html#line-highlighting)

<style>
.footnotes-sep {
  @apply mt-20 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

---

# Components

<div grid="~ cols-2 gap-4">
<div>

You can use Vue components directly inside your slides.

We have provided a few built-in components like `<Tweet/>` and `<Youtube/>` that you can use directly. And adding your custom components is also super easy.

```html
<Counter :count="10" />
```

<!-- ./components/Counter.vue -->
<Counter :count="10" m="t-4" />

Check out [the guides](https://sli.dev/builtin/components.html) for more.

</div>
<div>

```html
<Tweet id="1390115482657726468" />
```

<Tweet id="1390115482657726468" scale="0.65" />

</div>
</div>

<!--
Presenter note with **bold**, *italic*, and ~~striked~~ text.

Also, HTML elements are valid:
<div class="flex w-full">
  <span style="flex-grow: 1;">Left content</span>
  <span>Right content</span>
</div>
-->


---
class: px-20
---

# Themes

Slidev comes with powerful theming support. Themes can provide styles, layouts, components, or even configurations for tools. Switching between themes by just **one edit** in your frontmatter:

<div grid="~ cols-2 gap-2" m="-t-2">

```yaml
---
theme: default
---
```

```yaml
---
theme: seriph
---
```

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-default/01.png?raw=true">

<img border="rounded" src="https://github.com/slidevjs/themes/blob/main/screenshots/theme-seriph/01.png?raw=true">

</div>

Read more about [How to use a theme](https://sli.dev/themes/use.html) and
check out the [Awesome Themes Gallery](https://sli.dev/themes/gallery.html).

---
preload: false
---

# Animations

Animations are powered by [@vueuse/motion](https://motion.vueuse.org/).

```html
<div
  v-motion
  :initial="{ x: -80 }"
  :enter="{ x: 0 }">
  Slidev
</div>
```

<div class="w-60 relative mt-6">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-square.png"
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-circle.png"
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-triangle.png"
    />
  </div>

  <div
    class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Slidev
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x:35, y: 40, opacity: 0}"
  :enter="{ y: 0, opacity: 1, transition: { delay: 3500 } }">

[Learn More](https://sli.dev/guide/animations.html#motion)

</div>

---

# LaTeX

LaTeX is supported out-of-box powered by [KaTeX](https://katex.org/).

<br>

Inline $\sqrt{3x-1}+(1+x)^2$

Block
$$
\begin{array}{c}

\nabla \times \vec{\mathbf{B}} -\, \frac1c\, \frac{\partial\vec{\mathbf{E}}}{\partial t} &
= \frac{4\pi}{c}\vec{\mathbf{j}}    \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\

\nabla \times \vec{\mathbf{E}}\, +\, \frac1c\, \frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\

\nabla \cdot \vec{\mathbf{B}} & = 0

\end{array}
$$

<br>

[Learn more](https://sli.dev/guide/syntax#latex)

---

# Diagrams

You can create diagrams / graphs from textual descriptions, directly in your Markdown.

<div class="grid grid-cols-3 gap-10 pt-4 -mb-6">

```mermaid {scale: 0.5}
sequenceDiagram
    Alice->John: Hello John, how are you?
    Note over Alice,John: A typical interaction
```

```mermaid {theme: 'neutral', scale: 0.8}
graph TD
B[Text] --> C{Decision}
C -->|One| D[Result 1]
C -->|Two| E[Result 2]
```

```plantuml {scale: 0.7}
@startuml

package "Some Group" {
  HTTP - [First Component]
  [Another Component]
}

node "Other Groups" {
  FTP - [Second Component]
  [First Component] --> FTP
}

cloud {
  [Example 1]
}


database "MySql" {
  folder "This is my folder" {
    [Folder 3]
  }
  frame "Foo" {
    [Frame 4]
  }
}


[Another Component] --> [Example 1]
[Example 1] --> [Folder 3]
[Folder 3] --> [Frame 4]

@enduml
```

</div>

[Learn More](https://sli.dev/guide/syntax.html#diagrams)

---
src: ./pages/multiple-entries.md
hide: false
---

---
layout: center
class: text-center
---

# Learn More

[Documentations](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/showcases.html)
