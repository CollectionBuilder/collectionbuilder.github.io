# Homepage — Built Ons Section

Add this section to `index.html` **after** the existing Templates section (the `row` with the three template cards) and **before** the "Production" / philosophy section (the `row` with `bg-secondary`).

## Content

**Heading:** Built Ons

**Intro text:** Specialized frameworks built on CollectionBuilder that take it beyond digital collections — into essay writing, oral history analysis, and more.

### Card 1: CB-Essay

- **Header:** CB-Essay
- **Description:** A LONG-FORM DIGITAL SCHOLARSHIP FRAMEWORK for writing multimodal essays and monographs with integrated collection items
- **Button:** Learn about CB-Essay → `/built-ons/cb-essay.html`

### Card 2: Oral History as Data

- **Header:** Oral History as Data
- **Description:** AN ORAL HISTORY PUBLISHING AND ANALYSIS FRAMEWORK for visualizing coded interview transcripts as interactive digital collections
- **Button:** Learn about OHD → `/built-ons/ohd.html`

## Suggested HTML Structure

Follow the same pattern as the existing Templates section. Something like:

```html
<!-- Built Ons Section -->
<div class="row justify-content-center mt-4 px-3">
  <div class="col-md-10">
    <h2 class="text-center display-4" style="font-style: italic; font-family: Georgia, serif;">Built Ons</h2>
    <p class="text-center mb-2">
      Specialized frameworks built on CollectionBuilder that take it beyond digital collections — into essay writing, oral history analysis, and more.
    </p>
  </div>
</div>

<div class="row justify-content-center mt-3 px-3 mb-4">
  <!-- CB-Essay Card -->
  <div class="col-md-5 mb-3">
    <div class="card">
      <div class="card-header bg-dark text-white text-center py-3">
        <h3 class="mb-0" style="font-style: italic; font-family: Georgia, serif;">CB-Essay</h3>
      </div>
      <div class="card-body text-center">
        <p class="card-text">
          <em class="text-success">A LONG-FORM DIGITAL SCHOLARSHIP FRAMEWORK</em>
          for writing multimodal essays and monographs with integrated collection items
        </p>
        <a href="/built-ons/cb-essay.html" class="btn btn-primary btn-lg mt-2">Learn about CB-Essay</a>
      </div>
    </div>
  </div>

  <!-- OHD Card -->
  <div class="col-md-5 mb-3">
    <div class="card">
      <div class="card-header bg-dark text-white text-center py-3">
        <h3 class="mb-0" style="font-style: italic; font-family: Georgia, serif;">Oral History as Data</h3>
      </div>
      <div class="card-body text-center">
        <p class="card-text">
          <em class="text-success">AN ORAL HISTORY PUBLISHING AND ANALYSIS FRAMEWORK</em>
          for visualizing coded interview transcripts as interactive digital collections
        </p>
        <a href="/built-ons/ohd.html" class="btn btn-primary btn-lg mt-2">Learn about OHD</a>
      </div>
    </div>
  </div>
</div>
```

**Note:** The cards are `col-md-5` (not `col-md-4` like the three template cards) since there are only two Built Ons for now. This keeps them from looking too wide. When Digital Dramaturgy is added, switch to `col-md-4` for a three-across layout.
