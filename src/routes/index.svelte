<script>
  const fs = require("fs");
  import marked from "marked";

  const mdGlobalCode = fs.readFileSync("src/routes/global.md", "utf8");
  let globalCode = marked(mdGlobalCode);
</script>

<style>

</style>

<svelte:head>
  <title>✂️trim-css</title>
</svelte:head>

<h1>Trim Style System ✂️</h1>
<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2 mb="4">
      Light and forward thinking CSS library that uses attributes and variables
      for rapid theme prototyping.
    </h2>
    <ul mb="6">
      <li>⚡️ Light at &lt;10kb gzipped</li>
      <li>⛔️ No preprocessor required</li>
      <li>📐 Powerful grids & flexbox</li>
      <li>🌈 Customizable CSS variables</li>
    </ul>
    <a button href="https://unpkg.com/trim-css@0.0.2/dist/trim.min.css" mr="4">
      Download
    </a>
    <a button type="outline" href="https://github.com/atav1k/trim/pull/1">
      Contribute
    </a>
    <p mt="4">
      Trim draws syntactically from experimental frameworks like Raster and
      Shoelace. It uses CSS attributes to define components and utilities rather
      than classes, resembling JS props. For theming it relies on CSS variables
      which allows for rapid theme prototyping.
    </p>
  </li>
  <li cell span="4">
    <h2>Site variables</h2>
    {@html globalCode}
  </li>
</ul>

<h1 my="9">Utilities</h1>
<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Grid.css</h2>
    <p>
      Specifiy any number of grid columns from 1 to 24. Cells are initialized to
      one column but can span many. Default responsive behavior has all columns
      collapse to full width.
    </p>
    <code>
      &lt;ul grid columns="8" gap="2" /&gt;
      <br />
      &nbsp;&nbsp;&lt;li cell span="8" /&gt;
      <br />
      &lt;/grid&gt;
    </code>
  </li>
  <li cell span="6">
    <h2>4 column</h2>
    <ul grid mb="8" columns="4" class="h3">
      <li cell bg="gray3" p="3">cell</li>
      <li cell span="3" bg="gray4" p="4">3</li>
    </ul>
    <h2>7 column</h2>
    <ul grid mb="8" columns="7" class="h3">
      <li cell span="3" bg="gray3" p="4">3</li>
      <li cell span="4" bg="gray4" p="4">4</li>
    </ul>
    <h2>18 column</h2>
    <ul grid mb="8" columns="18" class="h3">
      <li cell span="3" bg="gray3" p="4">3</li>
      <li cell span="3" bg="gray4" p="4">3</li>
      <li cell span="3" bg="gray3" p="4">3</li>
      <li cell span="3" bg="gray4" p="4">3</li>
      <li cell span="6" bg="gray3" p="4">6</li>
    </ul>
    <h2>6 column with grid gap</h2>
    <ul grid columns="6" class="h3" gap="4">
      <li cell bg="gray3" p="4">cell</li>
      <li cell bg="gray4" p="4">cell</li>
      <li cell bg="gray3" p="4">cell</li>
      <li cell bg="gray4" p="4">cell</li>
      <li cell bg="gray3" p="4">cell</li>
      <li cell bg="gray4" p="4">cell</li>
    </ul>
  </li>
</ul>

<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Color.css</h2>
    <code>&lt;div color="white" bg="black" /&gt;</code>
  </li>
  <li cell span="6">
    <h2>Background</h2>
    <ul grid columns="2" class="h3" gap="2">
      <li cell bg="white" p="3">white</li>
      <li cell bg="black" color="white" p="3">black</li>
      <li cell bg="gray0" p="3">gray0</li>
      <li cell bg="gray1" p="3">gray1</li>
      <li cell bg="gray2" p="3">gray2</li>
      <li cell bg="gray3" p="3">gray3</li>
      <li cell bg="gray4" p="3">gray4</li>
      <li cell bg="gray5" p="3">gray5</li>
      <li cell bg="gray6" color="white" p="3">gray6</li>
      <li cell bg="gray7" color="white" p="3">gray7</li>
      <li cell bg="gray8" color="white" p="3">gray8</li>
      <li cell bg="gray9" color="white" p="3">gray9</li>
      <li cell bg="red" p="3">red</li>
      <li cell bg="pink" p="3">pink</li>
      <li cell bg="grape" p="3">grape</li>
      <li cell bg="violet" p="3">violet</li>
      <li cell bg="indigo" p="3">indigo</li>
      <li cell bg="blue" p="3">blue</li>
      <li cell bg="cyan" p="3">cyan</li>
      <li cell bg="teal" p="3">teal</li>
      <li cell bg="green" p="3">green</li>
      <li cell bg="lime" p="3">lime</li>
      <li cell bg="yellow" p="3">yellow</li>
      <li cell bg="orange" p="3">orange</li>
    </ul>
  </li>
</ul>

<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Position.css</h2>
    <code>&lt;h1 mx="4 sm2" my="sm2" p="2" /&gt;</code>
  </li>
  <li cell span="6">
    <h2>Padding</h2>
    <div px="8 sm4" py="2 sm9" bg="gray4" mb="8">Content</div>
    <h2 mt="8">Margin</h2>
    <div ml="12" bg="gray4">Content</div>
    <div mt="4" mr="8" bg="gray3">Content</div>
    <h2 mt="8">Responsive</h2>
    <p>
      Both margin and padding utilize and attribute that must be placed last.
    </p>
    <div ml="12 sm2" bg="gray4">Content</div>
    <div mt="4 sm8" mr="8" bg="gray3">Content</div>
  </li>
</ul>

<h1 my="9">Components</h1>
<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Alert.css</h2>
    <code>&lt;div alert type="primary" /&gt;</code>
  </li>
  <li cell span="6">
    <h2>Variations</h2>
    <ul grid gap="2" columns="1">
      <div alert>Alert</div>
      <div alert type="secondary">Alert</div>
      <div alert type="success">Alert</div>
      <div alert type="info">Alert</div>
      <div alert type="warning">Alert</div>
      <div alert type="danger">Alert</div>
      <div alert type="disabled">Alert</div>
    </ul>
  </li>
</ul>

<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Button.css</h2>
    <code>&lt;a button type="outline" href="." /&gt;</code>
  </li>
  <li cell span="6">
    <h2>Variations</h2>
    <ul grid columns="2" gap="2" flow="column" rows="5">
      <div button>Button</div>
      <div button disabled>Button</div>
      <div button type="outline">Button</div>
      <div button type="link">Button</div>
      <div button type="disabled">Button</div>
      <div button type="secondary">Button</div>
      <div button type="success">Button</div>
      <div button type="info">Button</div>
      <div button type="warning">Button</div>
      <div button type="danger">Button</div>
    </ul>
  </li>
</ul>

<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Chip.css</h2>
    <code>&lt;div chip type="primary" /&gt;</code>
  </li>
  <li cell span="6">
    <h2>Variations</h2>
    <ul grid columns="6" gap="2" flow="column" rows="4">
      <div chip>Chip</div>
      <div chip type="primary">Chip</div>
      <div chip type="secondary">Chip</div>
      <div chip type="success">Chip</div>
      <div chip type="info">Chip</div>
      <div chip type="warning">Chip</div>
      <div chip type="danger">Chip</div>
      <div chip type="disabled">Chip</div>
    </ul>
  </li>
</ul>

<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Form.css</h2>
  </li>
  <li cell span="6">
    <h2>Fields</h2>
    <ul grid columns="2" gap="2" mb="2">
      <li cell>
        <label>
          <input type="checkbox" />
          Checkbox
        </label>
        <br />
        <label>
          <input type="checkbox" />
          Checkbox
        </label>
        <br />
        <label>
          <input type="checkbox" />
          Checkbox
        </label>
      </li>
      <li>
        <label>
          <input type="radio" />
          Radio
        </label>
        <br />
        <label>
          <input type="radio" />
          Radio
        </label>
        <br />
        <label>
          <input type="radio" />
          Radio
        </label>
      </li>
    </ul>
    <ul grid columns="2" gap="2" flow="column" rows="3">
      <li cell>
        <select>
          <option>Item</option>
          <option>Item</option>
          <option>Item</option>
        </select>
      </li>
      <li cell>
        <input type="number" />
      </li>
      <li cell>
        <input type="file" />
      </li>
      <li cell>
        <input type="password" />
      </li>
      <li cell>
        <input type="time" />
      </li>
      <li cell>
        <textarea />
      </li>
    </ul>
  </li>
</ul>

<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Tab.css</h2>
    <code>&lt;div tab type="full"&gt;&lt;a /&gt;&lt;/div&gt;</code>
  </li>
  <li cell span="6">
    <h2>Variations</h2>
    <ul grid columns="2" gap="2" flow="column" rows="3">
      <div tab>
        <a href=".">Tab 1</a>
        <a href="." class="active">Active 2</a>
        <a href=".">Tab 3</a>
        <a href=".">Tab 4</a>
      </div>
      <div tab type="simple">
        <a href=".">Simple 1</a>
        <a href=".">Simple 2</a>
        <a href="." class="active">Simple 3</a>
        <a href=".">Simple 4</a>
      </div>
      <div tab type="full">
        <a href=".">Full 1</a>
        <a href=".">Full 2</a>
        <a href=".">Full 3</a>
        <a href="." class="active">Full 4</a>
      </div>
    </ul>
  </li>
</ul>

<ul grid columns="8" gap="8" my="9">
  <li cell span="2">
    <h2>Text.css</h2>
  </li>
  <li cell span="6">
    <h2>Headings</h2>
    <ul grid columns="2" gap="2" flow="column" rows="6">
      <li cell>
        <h1>Header 1</h1>
      </li>
      <li cell>
        <h2>Header 2</h2>
      </li>
      <li cell>
        <h3>Header 3</h3>
      </li>
      <li cell>
        <h4>Header 4</h4>
      </li>
      <li cell>
        <h5>Header 5</h5>
      </li>
      <li cell>
        <h6>Header 6</h6>
      </li>
      <li cell>
        <p>Paragraph</p>
      </li>
      <li cell>
        <small>Small</small>
      </li>
      <li cell>
        <code>Code</code>
      </li>
      <li cell>
        <a href=".">Link</a>
      </li>
      <li cell>
        <b>Bold</b>
      </li>
      <li>
        <div tooltip>
          tooltip
          <div tip>Some overlay text here</div>
        </div>
      </li>
    </ul>
  </li>
</ul>
