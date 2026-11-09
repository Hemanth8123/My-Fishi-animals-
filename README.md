doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#fff8e9">
  <title>MY FISHI ANIMALS</title>
  <style>
    :root {
      font-family: "Segoe UI", Arial, sans-serif;
      color: #242433;
      background: #fff8e9;
      font-synthesis: none;
      text-rendering: optimizeLegibility;
      scroll-behavior: smooth;
    }

    * {
      box-sizing: border-box;
    }

    body {
      min-width: 320px;
      margin: 0;
    }

    .page {
      width: min(1120px, calc(100% - 48px));
      margin: 0 auto;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      min-height: 82px;
    }

    .brand {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      text-decoration: none;
    }

    .brand-mark {
      display: block;
      width: 48px;
      height: 48px;
      flex: 0 0 auto;
    }

    .brand-name {
      color: #34284c;
      font-size: 0.96rem;
      font-weight: 900;
      letter-spacing: -0.045em;
      line-height: 1.05;
    }

    .brand-name span {
      display: block;
      color: #ed6a42;
    }

    nav {
      display: flex;
      align-items: center;
      gap: 26px;
    }

    nav a {
      color: #555466;
      font-size: 0.92rem;
      font-weight: 600;
      text-decoration: none;
    }

    nav a:hover {
      color: #ed6a42;
    }

    .hero {
      position: relative;
      overflow: hidden;
      display: grid;
      min-height: 420px;
      align-items: center;
      padding: 64px;
      border-radius: 28px;
      background: linear-gradient(115deg, #ffca65 0%, #ff8e72 52%, #ee6aa8 100%);
      isolation: isolate;
    }

    .hero::after {
      position: absolute;
      z-index: -1;
      right: -40px;
      bottom: -132px;
      width: 440px;
      height: 440px;
      border: 60px solid rgba(255, 255, 255, 0.2);
      border-radius: 50%;
      content: "";
    }

    .hero-copy {
      max-width: 580px;
    }

    .eyebrow {
      margin: 0 0 16px;
      color: #6e3c2b;
      font-size: 0.78rem;
      font-weight: 800;
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    h1 {
      margin: 0;
      color: #332640;
      font-size: clamp(3.2rem, 8vw, 6.5rem);
      letter-spacing: -0.08em;
      line-height: 0.94;
    }

    .hero-copy > p:not(.eyebrow) {
      max-width: 470px;
      margin: 23px 0 0;
      color: #533c45;
      font-size: 1.08rem;
      line-height: 1.7;
    }

    .button {
      display: inline-flex;
      min-height: 48px;
      align-items: center;
      justify-content: center;
      margin-top: 25px;
      padding: 0 21px;
      border-radius: 999px;
      background: #332640;
      color: #fff;
      font-size: 0.93rem;
      font-weight: 700;
      text-decoration: none;
      transition: transform 160ms ease, background 160ms ease;
    }

    .button:hover {
      transform: translateY(-2px);
      background: #4a3560;
    }

    .content {
      padding: 78px 0 0;
    }

    .section-heading {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 24px;
      margin-bottom: 25px;
    }

    .section-heading .eyebrow {
      margin-bottom: 9px;
      color: #6a55c7;
    }

    h2 {
      margin: 0;
      font-size: clamp(2rem, 4vw, 2.8rem);
      letter-spacing: -0.065em;
    }

    .section-note {
      max-width: 390px;
      margin: 0 0 3px;
      color: #6c6a79;
      line-height: 1.6;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 20px;
    }

    .card {
      overflow: hidden;
      border: 1px solid rgba(52, 43, 71, 0.08);
      border-radius: 20px;
      background: #fff;
      box-shadow: 0 12px 30px rgba(58, 44, 71, 0.06);
    }

    .card img {
      display: block;
      width: 100%;
      height: 210px;
      object-fit: cover;
      background: #eee8f8;
    }

    .card-body {
      padding: 21px 22px 24px;
    }

    .tag {
      display: inline-block;
      padding: 6px 10px;
      border-radius: 999px;
      background: #eee8ff;
      color: #5a43ad;
      font-size: 0.72rem;
      font-weight: 800;
      letter-spacing: 0.05em;
      text-transform: uppercase;
    }

    .card:nth-child(3n + 2) .tag {
      background: #e4f5d6;
      color: #3c702a;
    }

    .card:nth-child(3n) .tag {
      background: #ffead9;
      color: #a34a24;
    }

    h3 {
      margin: 14px 0 8px;
      font-size: 1.2rem;
      letter-spacing: -0.035em;
    }

    .card p {
      margin: 0;
      color: #6c6a79;
      font-size: 0.93rem;
      line-height: 1.65;
    }

    .explorer {
      padding-top: 72px;
    }

    .catalog-toolbar {
      display: grid;
      grid-template-columns: minmax(220px, 1fr) minmax(180px, 0.45fr);
      gap: 14px;
      margin: 24px 0 12px;
    }

    .catalog-toolbar input,
    .catalog-toolbar select {
      width: 100%;
      min-height: 48px;
      padding: 0 14px;
      border: 1px solid #e3ddeb;
      border-radius: 12px;
      background: #fff;
      color: #332640;
      font: inherit;
    }

    .catalog-toolbar input:focus,
    .catalog-toolbar select:focus {
      border-color: #6a55c7;
      outline: 3px solid rgba(106, 85, 199, 0.16);
    }

    .catalog-status {
      min-height: 26px;
      margin: 0 0 16px;
      color: #6c6a79;
      font-size: 0.88rem;
    }

    .catalog-pager {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 16px;
      margin-top: 24px;
    }

    .catalog-pager button {
      min-height: 42px;
      padding: 0 16px;
      border: 0;
      border-radius: 999px;
      background: #6a55c7;
      color: #fff;
      cursor: pointer;
      font: inherit;
      font-weight: 700;
    }

    .catalog-pager button:disabled {
      cursor: not-allowed;
      opacity: 0.45;
    }

    .catalog-page-number {
      color: #6c6a79;
      font-size: 0.88rem;
    }

    .catalog-card .card img {
      height: 230px;
    }

    .catalog-card .card-body {
      display: grid;
      gap: 9px;
    }

    .catalog-card h3 {
      margin: 3px 0 0;
    }

    .catalog-card .scientific-name {
      margin: -5px 0 0;
      color: #777383;
      font-size: 0.88rem;
      font-style: italic;
    }

    .catalog-card .catalog-facts {
      margin: 0;
      color: #6c6a79;
      font-size: 0.85rem;
      line-height: 1.55;
    }

    .catalog-credit,
    .catalog-link {
      color: #6650bd;
      font-size: 0.78rem;
      line-height: 1.5;
      overflow-wrap: anywhere;
    }

    .catalog-credit {
      color: #777383;
    }

    .catalog-card details {
      padding-top: 9px;
      border-top: 1px solid #ece9f0;
      color: #555466;
      font-size: 0.86rem;
      line-height: 1.6;
    }

    .catalog-card summary {
      color: #5a43ad;
      cursor: pointer;
      font-weight: 700;
    }

    .catalog-card details p {
      margin-top: 8px;
      color: #6c6a79;
      font-size: 0.86rem;
    }

    .catalog-empty {
      grid-column: 1 / -1;
      padding: 30px;
      border: 1px dashed #d9d2e8;
      border-radius: 16px;
      color: #6c6a79;
      text-align: center;
    }

    .sr-only {
      position: absolute;
      overflow: hidden;
      width: 1px;
      height: 1px;
      padding: 0;
      border: 0;
      clip: rect(0, 0, 0, 0);
      white-space: nowrap;
      clip-path: inset(50%);
    }

    footer {
      display: flex;
      justify-content: space-between;
      gap: 16px;
      margin-top: 78px;
      padding: 22px 0 28px;
      border-top: 1px solid #e8dfd3;
      color: #777383;
      font-size: 0.84rem;
    }

    @media (max-width: 760px) {
      .hero {
        min-height: 370px;
        padding: 42px;
      }

      .cards {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .catalog-toolbar {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 560px) {
      .page {
        width: min(100% - 32px, 460px);
      }

      header {
        min-height: 72px;
        flex-wrap: wrap;
        gap: 12px;
        padding: 12px 0;
      }

      nav {
        gap: 16px;
      }

      nav a {
        font-size: 0.86rem;
      }

      .hero {
        min-height: 360px;
        padding: 30px 24px;
        border-radius: 22px;
      }

      .hero::after {
        right: -180px;
        bottom: -190px;
      }

      .content {
        padding-top: 58px;
      }

      .section-heading {
        align-items: start;
        flex-direction: column;
        gap: 8px;
      }

      .cards {
        grid-template-columns: 1fr;
        gap: 15px;
      }

      .catalog-pager {
        gap: 10px;
      }

      .catalog-pager button {
        padding: 0 12px;
      }

      .card img {
        height: 220px;
      }

      footer {
        flex-direction: column;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      :root {
        scroll-behavior: auto;
      }

      *,
      *::before,
      *::after {
        transition-duration: 0.01ms !important;
      }
    }
  </style>
</head>
<body>
  <div class="page">
    <header>
      <a class="brand" href="#" aria-label="MY FISHI ANIMALS home">
        <svg class="brand-mark" viewBox="0 0 64 64" role="img" aria-labelledby="logo-title">
          <title id="logo-title">Fish and animal logo</title>
          <defs>
            <linearGradient id="logo-water" x1="0" y1="0" x2="1" y2="1">
              <stop offset="0" stop-color="#55c9d4"/>
              <stop offset="1" stop-color="#6a55c7"/>
            </linearGradient>
          </defs>
          <circle cx="32" cy="32" r="30" fill="#fff0d6"/>
          <path d="M7 34c8-11 20-13 31-6l12-9v28l-12-9C27 45 15 43 7 34Z" fill="url(#logo-water)"/>
          <circle cx="17" cy="32" r="2" fill="#fff"/>
          <circle cx="17" cy="32" r="1" fill="#34284c"/>
          <path d="M40 43c2-7 8-11 16-11-8 0-14-4-16-11" fill="none" stroke="#ed6a42" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"/>
          <path d="M10 49c5 3 10 3 15 0" fill="none" stroke="#ff9e59" stroke-linecap="round" stroke-width="3"/>
        </svg>
        <span class="brand-name">MY FISHI <span>ANIMALS</span></span>
      </a>
      <nav aria-label="Main navigation">
        <a href="#fish">Fish</a>
        <a href="#animals">Animals</a>
      </nav>
    </header>

    <main>
      <section class="hero" aria-labelledby="page-title">
        <div class="hero-copy">
          <p class="eyebrow">Curious minds welcome</p>
          <h1 id="page-title">Meet the<br>wild ones.</h1>
          <p>Swim beneath the waves and wander into the animal kingdom. There is always something wonderful to discover.</p>
          <a class="button" href="#fish">Start exploring <span aria-hidden="true">&nbsp;↓</span></a>
        </div>
      </section>

      <section class="content explorer" id="explore" aria-labelledby="explore-title">
        <div class="section-heading">
          <div>
            <p class="eyebrow">A living species guide</p>
            <h2 id="explore-title">Explore 1,000+ species</h2>
          </div>
          <p class="section-note">Browse thousands of real fish and animal species, see their photos, scientific names, observation records, and more facts. The fish filter focuses on bony fish; the full catalog includes other animal groups too.</p>
        </div>
        <div class="catalog-toolbar">
          <label>
            <span class="sr-only">Search species</span>
            <input id="species-search" type="search" placeholder="Search common or scientific names" autocomplete="off">
          </label>
          <label>
            <span class="sr-only">Choose species group</span>
            <select id="species-group">
              <option value="all">All animals and fish</option>
              <option value="fish">Fish (bony fish)</option>
            </select>
          </label>
        </div>
        <p class="catalog-status" id="catalog-status" role="status" aria-live="polite">Loading species catalog…</p>
        <div class="cards" id="catalog-cards" aria-live="polite"></div>
        <div class="catalog-pager" aria-label="Species catalog pages">
          <button id="previous-page" type="button" disabled>Previous</button>
          <span class="catalog-page-number" id="page-number">Page 1</span>
          <button id="next-page" type="button" disabled>Next</button>
        </div>
        <p class="catalog-credit">Species and photo data from <a href="https://www.inaturalist.org/" target="_blank" rel="noopener noreferrer">iNaturalist</a>. Photo creators and license details are credited on each card. Additional species facts are linked from Wikipedia.</p>
      </section>

      <section class="content" id="fish" aria-labelledby="fish-title">
        <div class="section-heading">
          <div>
            <p class="eyebrow">Under the surface</p>
            <h2 id="fish-title">Fantastic fish</h2>
          </div>
          <p class="section-note">From colorful reefs to quiet freshwater streams, fish come in an amazing range of shapes and sizes.</p>
        </div>
        <div class="cards">
          <article class="card">
            <img src="https://images.unsplash.com/photo-1535591273668-578e31182c4f?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="Bright tropical fish swimming among coral" loading="lazy">
            <div class="card-body">
              <span class="tag">Coral reef</span>
              <h3>Clownfish</h3>
              <p>These orange-and-white reef fish live among sea anemones, whose stinging tentacles help protect them from predators.</p>
            </div>
          </article>
          <article class="card">
            <img src="https://images.unsplash.com/photo-1524704654690-b56c05c78a00?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="A vivid blue fish in clear water" loading="lazy">
            <div class="card-body">
              <span class="tag">Ocean traveler</span>
              <h3>Blue tang</h3>
              <p>Known for its bold blue color and yellow tail, the blue tang grazes on algae around warm Indo-Pacific reefs.</p>
            </div>
          </article>
          <article class="card">
            <img src="https://images.unsplash.com/photo-1522069169874-c58ec4b76be5?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="A school of small fish moving together underwater" loading="lazy">
            <div class="card-body">
              <span class="tag">Freshwater</span>
              <h3>Life in a school</h3>
              <p>Many small fish swim in groups called schools. Moving together can make it harder for predators to single one out.</p>
            </div>
          </article>
        </div>
      </section>

      <section class="content" id="animals" aria-labelledby="animals-title">
        <div class="section-heading">
          <div>
            <p class="eyebrow">On land and in the sky</p>
            <h2 id="animals-title">Amazing animals</h2>
          </div>
          <p class="section-note">Every habitat is home to remarkable creatures, each with its own special way of life.</p>
        </div>
        <div class="cards">
          <article class="card">
            <img src="https://images.unsplash.com/photo-1549366021-9f761d450615?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="An elephant walking through a grassy landscape" loading="lazy">
            <div class="card-body">
              <span class="tag">Savanna</span>
              <h3>Elephants</h3>
              <p>Elephants use their trunks to smell, drink, gather food, and communicate with members of their close-knit herds.</p>
            </div>
          </article>
          <article class="card">
            <img src="https://images.unsplash.com/photo-1561731216-c3a4d99437d5?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="A tiger resting among green plants" loading="lazy">
            <div class="card-body">
              <span class="tag">Forest</span>
              <h3>Tigers</h3>
              <p>Each tiger has a unique stripe pattern. These powerful cats are excellent swimmers and usually hunt alone.</p>
            </div>
          </article>
          <article class="card">
            <img src="https://images.unsplash.com/photo-1552728089-57bdde30beb3?auto=format&amp;fit=crop&amp;w=1000&amp;q=85" alt="A colorful parrot perched on a branch" loading="lazy">
            <div class="card-body">
              <span class="tag">Rainforest</span>
              <h3>Parrots</h3>
              <p>Parrots use strong curved beaks to crack seeds and nuts. Many species are social and communicate with lively calls.</p>
            </div>
          </article>
        </div>
      </section>
    </main>

    <footer>
      <span>Stay curious. Be kind to wildlife.</span>
      <span>MY FISHI ANIMALS · Done by Hemanth Babu</span>
    </footer>
  </div>
  <script>
    const catalogSize = 24;
    const catalogState = {
      page: 1,
      total: 0,
      controller: null,
      requestId: 0,
      timer: null
    };
    const catalogStatus = document.getElementById("catalog-status");
    const catalogCards = document.getElementById("catalog-cards");
    const searchInput = document.getElementById("species-search");
    const groupSelect = document.getElementById("species-group");
    const previousButton = document.getElementById("previous-page");
    const nextButton = document.getElementById("next-page");
    const numberFormat = new Intl.NumberFormat();

    function makeLink(text, href, className) {
      const link = document.createElement("a");
      link.className = className || "catalog-link";
      link.href = href;
      link.target = "_blank";
      link.rel = "noopener noreferrer";
      link.textContent = text;
      return link;
    }

    function makeCatalogCard(taxon) {
      const article = document.createElement("article");
      article.className = "card catalog-card";

      const photo = taxon.default_photo;
      if (photo) {
        const image = document.createElement("img");
        image.src = photo.medium_url || photo.square_url;
        image.alt = (taxon.preferred_common_name || taxon.name) + " photo";
        image.loading = "lazy";
        image.addEventListener("error", function () {
          image.remove();
        }, { once: true });
        article.appendChild(image);
      }

      const body = document.createElement("div");
      body.className = "card-body";

      const tag = document.createElement("span");
      tag.className = "tag";
      tag.textContent = taxon.iconic_taxon_name || "Wildlife";
      const heading = document.createElement("h3");
      heading.textContent = taxon.preferred_common_name || taxon.name;
      const scientificName = document.createElement("p");
      scientificName.className = "scientific-name";
      scientificName.textContent = taxon.name;
      const facts = document.createElement("p");
      facts.className = "catalog-facts";
      facts.textContent = numberFormat.format(taxon.observations_count || 0) +
        " community observations" +
        (taxon.conservation_status && taxon.conservation_status.status_name
          ? " · " + taxon.conservation_status.status_name
          : "");

      body.append(tag, heading, scientificName, facts);

      const taxonUrl = "https://www.inaturalist.org/taxa/" + encodeURIComponent(taxon.id);
      body.appendChild(makeLink("View species on iNaturalist", taxonUrl));

      if (photo) {
        const credit = document.createElement("p");
        credit.className = "catalog-credit";
        credit.textContent = "Photo: " + (photo.attribution || "iNaturalist contributor") +
          " · " + (photo.license_code || "License not listed");
        body.appendChild(credit);
        body.appendChild(makeLink(
          "Photo and license details",
          "https://www.inaturalist.org/photos/" + encodeURIComponent(photo.id),
          "catalog-credit"
        ));
      }

      const details = document.createElement("details");
      const summary = document.createElement("summary");
      summary.textContent = "More facts";
      const description = document.createElement("p");
      description.textContent = "Open for a species description.";
      details.append(summary, description);
      let factsLoaded = false;
      details.addEventListener("toggle", async function () {
        if (!details.open || factsLoaded) {
          return;
        }
        factsLoaded = true;
        const wikipediaUrl = taxon.wikipedia_url;
        if (!wikipediaUrl) {
          description.textContent = "No Wikipedia summary is linked for this species yet.";
          return;
        }

        try {
          const articleUrl = new URL(wikipediaUrl);
          if (articleUrl.hostname !== "en.wikipedia.org" &&
              !articleUrl.hostname.endsWith(".wikipedia.org")) {
            throw new Error("Unrecognized encyclopedia link.");
          }
          const title = decodeURIComponent(articleUrl.pathname.split("/").pop()).replace(/_/g, " ");
          const summaryUrl = "https://en.wikipedia.org/api/rest_v1/page/summary/" +
            encodeURIComponent(title);
          const response = await fetch(summaryUrl);
          if (!response.ok) {
            throw new Error("Encyclopedia summary unavailable.");
          }
          const article = await response.json();
          description.textContent = article.extract ||
            "No additional description is available for this species.";
          if (article.content_urls && article.content_urls.desktop &&
              article.content_urls.desktop.page) {
            details.appendChild(makeLink("Read the Wikipedia article", article.content_urls.desktop.page));
          }
        } catch (error) {
          description.textContent = error.message +
            " You can still open the species page on iNaturalist for more information.";
        }
      });
      body.appendChild(details);
      article.appendChild(body);
      return article;
    }

    function updatePager() {
      const lastPage = Math.max(1, Math.ceil(catalogState.total / catalogSize));
      document.getElementById("page-number").textContent =
        "Page " + catalogState.page + " of " + numberFormat.format(lastPage);
      previousButton.disabled = catalogState.page <= 1;
      nextButton.disabled = catalogState.page >= lastPage;
    }

    async function loadCatalog() {
      const requestId = ++catalogState.requestId;
      if (catalogState.controller) {
        catalogState.controller.abort();
      }
      catalogState.controller = new AbortController();
      const params = new URLSearchParams({
        taxon_id: groupSelect.value === "fish" ? "47178" : "1",
        rank: "species",
        is_active: "true",
        photos: "true",
        per_page: String(catalogSize),
        page: String(catalogState.page),
        order: "desc",
        order_by: "observations_count"
      });
      const query = searchInput.value.trim();
      if (query) {
        params.set("q", query);
      }

      catalogStatus.textContent = "Loading species and photos…";
      catalogCards.replaceChildren();
      previousButton.disabled = true;
      nextButton.disabled = true;

      try {
        const response = await fetch("https://api.inaturalist.org/v1/taxa?" + params, {
          signal: catalogState.controller.signal
        });
        if (!response.ok) {
          throw new Error("Species catalog request failed (" + response.status + ").");
        }
        const data = await response.json();
        if (requestId !== catalogState.requestId) {
          return;
        }
        catalogState.total = data.total_results;
        if (!data.results.length) {
          const empty = document.createElement("p");
          empty.className = "catalog-empty";
          empty.textContent = "No species matched that search. Try another name.";
          catalogCards.appendChild(empty);
        } else {
          catalogCards.replaceChildren(...data.results.map(makeCatalogCard));
        }
        const firstResult = (catalogState.page - 1) * catalogSize + 1;
        const lastResult = Math.min(catalogState.page * catalogSize, catalogState.total);
        catalogStatus.textContent = catalogState.total
          ? "Showing " + numberFormat.format(firstResult) + "–" +
            numberFormat.format(lastResult) + " of " +
            numberFormat.format(catalogState.total) + " species."
          : "No species found.";
        updatePager();
      } catch (error) {
        if (error.name === "AbortError" || requestId !== catalogState.requestId) {
          return;
        }
        catalogStatus.textContent =
          "Could not load the species catalog: " + error.message +
          " Check your internet connection and try again.";
        catalogCards.replaceChildren();
        updatePager();
      }
    }

    searchInput.addEventListener("input", function () {
      window.clearTimeout(catalogState.timer);
      catalogState.page = 1;
      catalogState.timer = window.setTimeout(loadCatalog, 350);
    });

    groupSelect.addEventListener("change", function () {
      catalogState.page = 1;
      loadCatalog();
    });

    previousButton.addEventListener("click", function () {
      if (catalogState.page > 1) {
        catalogState.page -= 1;
        loadCatalog();
      }
    });

    nextButton.addEventListener("click", function () {
      if (catalogState.page < Math.ceil(catalogState.total / catalogSize)) {
        catalogState.page += 1;
        loadCatalog();
      }
    });

    loadCatalog();
  </script>
</body>
</html>
