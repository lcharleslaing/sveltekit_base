<script>
  import Accordion from "$lib/components/Accordion.svelte";

  let bible_book = "";
  let bible_chapter = "";

  // create api url that includes bible_book and bible_chapter
  let api_url =
    "https://labs.bible.org/api/?passage=" + bible_book + bible_chapter;

  // fetch api data
  fetch(api_url)
    .then((response) => response.json())
    .then((data) => {
      // create a new accordion component
      let accordion = new Accordion({
        target: document.body,
        props: {
          title: "Bible Verse",
          content: data.text,
        },
      });
    });
</script>

<br />
<h1 class="center">Bible</h1>
<br />

<!-- input with a submit button inline -->
<form>
  <input type="text" name="input" />
  <input type="submit" value="Search" />
</form>

<Accordion class="accordion" />

<style>
  .center {
    text-align: center;
  }
  form {
    /* center form horizontally  */
    display: inline-block;
    text-align: center;
    /* input width 100% */
    width: 100%;
  }
  .accordion {
    width: 100%;
    margin-top: 10px;
  }
</style>
