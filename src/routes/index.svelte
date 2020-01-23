<script>

</script>

<style>

</style>

<svelte:head>
  <title>✂️trim-css</title>
</svelte:head>

<h1>✂️ Trim CSS Tester</h1>
<p>A sample page to make sure Trim behaves well while under development.</p>
<grid columns="8" gap="8" mt="8">
  <cell span="2">
    <h2>Grid</h2>
    <p>
      Specifiy any number of columns within a grid from 1 to 24. Cells are
      initialized to one column but can span many.
    </p>
    <code>
      &lt;grid columns="8" gap="2" /&gt;
      <br />
      &nbsp;&nbsp;&lt;cell span="8" /&gt;
      <br />
      &lt;/grid&gt;
    </code>
  </cell>
  <cell span="6">
    <h2>4 column</h2>
    <grid mb="8" columns="4" class="h3">
      <cell bg="gray3" p="3">cell</cell>
      <cell span="3" bg="gray4" p="4">3</cell>
    </grid>
    <h2>7 column</h2>
    <grid mb="8" columns="7" class="h3">
      <cell span="3" bg="gray3" p="4">3</cell>
      <cell span="4" bg="gray4" p="4">4</cell>
    </grid>
    <h2>18 column</h2>
    <grid mb="8" columns="18" class="h3">
      <cell span="3" bg="gray3" p="4">3</cell>
      <cell span="3" bg="gray4" p="4">3</cell>
      <cell span="3" bg="gray3" p="4">3</cell>
      <cell span="3" bg="gray4" p="4">3</cell>
      <cell span="6" bg="gray3" p="4">6</cell>
    </grid>
    <h2>6 column with grid gap</h2>
    <grid mb="8" columns="6" class="h3" gap="4">
      <cell bg="gray3" p="4">cell</cell>
      <cell bg="gray4" p="4">cell</cell>
      <cell bg="gray3" p="4">cell</cell>
      <cell bg="gray4" p="4">cell</cell>
      <cell bg="gray3" p="4">cell</cell>
      <cell bg="gray4" p="4">cell</cell>
    </grid>
  </cell>
</grid>

<grid columns="8" gap="8" mt="8">
  <cell span="2">
    <h2>Color</h2>
    <p>Use open color for background and body.</p>
    <code>&lt;div color="white" bg="black" /&gt;</code>
  </cell>
  <cell span="6">
    <h2>Background</h2>
    <grid mb="8" columns="2" class="h3" gap="2">
      <cell bg="white" p="3">white</cell>
      <cell bg="black" color="white" p="3">black</cell>
      <cell bg="gray0" p="3">gray0</cell>
      <cell bg="gray1" p="3">gray1</cell>
      <cell bg="gray2" p="3">gray2</cell>
      <cell bg="gray3" p="3">gray3</cell>
      <cell bg="gray4" p="3">gray4</cell>
      <cell bg="gray5" p="3">gray5</cell>
      <cell bg="gray6" color="white" p="3">gray6</cell>
      <cell bg="gray7" color="white" p="3">gray7</cell>
      <cell bg="gray8" color="white" p="3">gray8</cell>
      <cell bg="gray9" color="white" p="3">gray9</cell>
      <cell bg="red" p="3">red</cell>
      <cell bg="pink" p="3">pink</cell>
      <cell bg="grape" p="3">grape</cell>
      <cell bg="violet" p="3">violet</cell>
      <cell bg="indigo" p="3">indigo</cell>
      <cell bg="blue" p="3">blue</cell>
      <cell bg="cyan" p="3">cyan</cell>
      <cell bg="teal" p="3">teal</cell>
      <cell bg="green" p="3">green</cell>
      <cell bg="lime" p="3">lime</cell>
      <cell bg="yellow" p="3">yellow</cell>
      <cell bg="orange" p="3">orange</cell>
    </grid>
  </cell>
</grid>

<grid columns="8" gap="8" mt="8">
  <cell span="2">
    <h2>Positioning</h2>
    <p>Use margin and padding.</p>
    <code>&lt;h1 mx="4 sm2" my="sm2" p="2" /&gt;</code>
  </cell>
  <cell span="6">
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
  </cell>
</grid>

<grid columns="8" gap="8" mt="8">
  <cell span="2">
    <h2>Text</h2>
    <p>Use margin and padding.</p>
  </cell>
  <cell span="6">
    <h2>Headings</h2>
    <grid mb="8" columns="2" gap="2" flow="column" rows="6">
      <cell>
        <h1>Header 1</h1>
      </cell>
      <cell>
        <h2>Header 2</h2>
      </cell>
      <cell>
        <h3>Header 3</h3>
      </cell>
      <cell>
        <h4>Header 4</h4>
      </cell>
      <cell>
        <h5>Header 5</h5>
      </cell>
      <cell>
        <h6>Header 6</h6>
      </cell>
      <cell>
        <p>Paragraph</p>
      </cell>
      <cell>
        <small>Small</small>
      </cell>
      <cell>
        <code>Code</code>
      </cell>
      <cell>
        <a href=".">Link</a>
      </cell>
      <cell>
        <b>Bold</b>
      </cell>
    </grid>
  </cell>
</grid>
