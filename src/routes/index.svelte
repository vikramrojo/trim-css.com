<script>

</script>

<style>

</style>

<svelte:head>
  <title>✂️trim-css</title>
</svelte:head>

<h1>✂️ Trim CSS Tester</h1>
<p>A sample page to make sure Trim behaves well while under development.</p>
<ul grid columns="8" gap="8" mt="8">
  <li cell span="2">
    <h2>Grid</h2>
    <p>
      Specifiy any number of columns within a grid from 1 to 24. Cells are
      initialized to one column but can span many.
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
    <ul grid mb="8" columns="6" class="h3" gap="4">
      <li cell bg="gray3" p="4">cell</li>
      <li cell bg="gray4" p="4">cell</li>
      <li cell bg="gray3" p="4">cell</li>
      <li cell bg="gray4" p="4">cell</li>
      <li cell bg="gray3" p="4">cell</li>
      <li cell bg="gray4" p="4">cell</li>
    </ul>
  </li>
</ul>

<ul grid columns="8" gap="8" mt="8">
  <li cell span="2">
    <h2>Color</h2>
    <p>Use open color for background and body.</p>
    <code>&lt;div color="white" bg="black" /&gt;</code>
  </li>
  <li cell span="6">
    <h2>Background</h2>
    <ul grid mb="8" columns="2" class="h3" gap="2">
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

<ul grid columns="8" gap="8" mt="8">
  <li cell span="2">
    <h2>Positioning</h2>
    <p>Use margin and padding.</p>
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

<ul grid columns="8" gap="8" mt="8">
  <li cell span="2">
    <h2>Text</h2>
    <p>Use margin and padding.</p>
  </li>
  <li cell span="6">
    <h2>Headings</h2>
    <ul grid mb="8" columns="2" gap="2" flow="column" rows="6">
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
    </ul>
  </li>
</ul>
