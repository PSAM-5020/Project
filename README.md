# Project

### Goal
The goal of this project is to examine the experience of art and identity through how these topics are characterized by both artists and institutions. Through extracting core ideas from texts authored by both artists and institutions, pattern analysis can expose what pieces make up the persona of identity that an artist expresses in their work for those whose identity spans across traditional labels and constrained classifications.

### Data
The data for this project is manually curated. The collection process begins with art exhibitions dated after 2000 that are curated around the experience of mixed-race and Asian American identity and extracts artists involved whose work is catalogued by major U. S. art insitutions' open access archives. Then, data on these artists is collected from public artist statements and interviews and combined with those institutional records.

Data considered includes records from the following museums, selected from Art Newspaper's list of most visited art museums in [2025](https://airtable.com/appc8C2UnLN7h7Raj/shr2Bt263MOCBFZkq/tblUb1qPQA5AXrBTG?viewControls=on) and filtered to museums in the United States that have open access archives or databases available online - numbered by their position in this visitor-ranked list
5. Metropolitan Museum of Art, New York, NY - 5,984,091 visitors
18. National Gallery of Art, Washington, D. C. - 2,847,587 visitors
19. Museum of Modern Art, New York, NY - 2,763,720 visitors
48. Art Insitute of Chicago, Chicago, IL - 1,503,406 visitors
57. J. Paul Getty Center, Los Angeles, CA - 1,323,616 visitors
80. Smithsonian Insitution, Washington, D. C. - 937,716 visitors
86. Whitney Museum of American Art, New York, NY - 885,360 visitors
100. Cleveland Museum of Art, Cleveland, OH - 800,822 visitors

The updated sampling of data collected is available [here](https://github.com/PSAM-5020/Project/tree/main/data/downloaded/processed).

### Process outline
1. Collect data (:white_check_mark:)
  A. Public artist statements, interviews, artwork titles, and institutional biographical text will be the data considered for the analysis
2. Clean and standardize data (**reusable processes built** :white_check_mark:)
3. Modeling (Processes built :white_check_mark: _Tuning in progress_)
  Using [nomic-embed-text-v1.5](https://huggingface.co/nomic-ai/nomic-embed-text-v1.5):
  A. Split texts by semantic chunks to get 1-3 sentences about same subject
  B. Use search_document with terms to filter resulting semantic chunks and keep only those about identity
  C. Embed texts
  D. Cluster using k-means to group texts by theme, examine and evaluate results
     Current progress:
     <img width="1006" height="867" alt="Screenshot 2026-04-15 at 1 07 28 PM" src="https://github.com/user-attachments/assets/03d71ce6-57db-4c9a-9f67-05b0bebddcea" />

  E. Use TF-IDF to get words from all the text in a cluster that "summarize" that cluster
5. Average the text clusters to summarize artists based on their text clustering and embeddings, format to plot on the UI (:white_check_mark:)
6. Manually examine clusters and labels to get final cluster labels that will display on UI (**_In progress_**)
   Summary of all extracted labels, filtered down to those about identity manually:
   <img width="1571" height="635" alt="Screenshot 2026-04-25 at 5 01 56 PM" src="https://github.com/user-attachments/assets/36b75370-13ff-43f1-aebe-5d6ba1827e23" />
7. Visually plot clusters and breakdown of themes over time per artists - see prototype [here](https://mnav0.github.io/thesis/) (**_In progress_**)
  ** Note: right now I'm plotting all of the exported clusters with different values for _n_, this is more exploratory for me to visually understand the results but the final visualization will likely have a couple of versions of these clusters that are combined with the different sources to get a sense of different label/term associations possible with different number of groupings (see below for current progress)
  <img width="1527" height="764" alt="Screenshot 2026-04-25 at 5 03 33 PM" src="https://github.com/user-attachments/assets/ed51d43b-473d-4d39-b32e-4a0fac1d16d7" />


