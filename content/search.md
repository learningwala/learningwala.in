---
title: "Search"
---

<div id="pagefind-search"></div>

<link href="/pagefind/pagefind-ui.css" rel="stylesheet">
<script src="/pagefind/pagefind-ui.js"></script>

<script>
  window.addEventListener("DOMContentLoaded", () => {
    new PagefindUI({
      element: "#pagefind-search",
      showSubResults: true,
      autofocus: true
    });
  });
</script>

<script>
  document.addEventListener("keydown", function (e) {
    if ((e.metaKey || e.ctrlKey) && e.key.toLowerCase() === "k") {
      e.preventDefault();
      window.location.href = "/search/";
    }
  });
</script>
