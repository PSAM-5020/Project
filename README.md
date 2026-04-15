# Project

### Goal
The goal of this project is to examine the experience of art and identity through how these topics are characterized by both artists and institutions. Through extracting core ideas from texts authored by both artists and institutions, pattern analysis can expose what pieces make up the persona of identity that an artist expresses in their work for those whose identity spans across traditional labels and constrained classifications.

### Data
The data for this project is manually curated. The collection process begins with art exhibitions dated after 2000 that are curated around the experience of mixed-race and Asian American identity and extracts artists involved whose work is catalogued by major U. S. art insitutions' open access archives. Then, data on these artists is collected from public artist statements and interviews and combined with those institutional records.

Data considered includes records from the following museums (selected from Art Newspaper's list of most visited art museums in [2023](https://www.theartnewspaper.com/2024/03/26/the-100-most-popular-art-museums-in-the-world-2023)/[2024](https://www.theartnewspaper.com/2025/04/01/the-worlds-most-visited-museums-2024-) and filtered to museums in the United States that have open access archives or databases available online)
1. Smithsonian Insitution, Washington, D. C.
2. Metropolitan Museum of Art, New York, NY
3. Whitney Museum of American Art, New York, NY
4. Museum of Modern Art, New York, NY
5. J. Paul Getty Center, Los Angeles, CA
6. Art Insitute of Chicago, Chicago, IL
7. Cleveland Museum of Art, Cleveland, OH

The updated sampling of data collected is available [here](https://github.com/PSAM-5020/Project/tree/main/data/downloaded/processed).

### Process outline
1. Collect data
  A. Public artist statements, interviews, artwork titles, and institutional biographical text will be the data considered for the analysis (**_In progress_**)
2. Clean and standardize data (**reusable processes built** :white_check_mark:)
3. Modeling (_In progress_)
  Using [nomic-embed-text-v1.5](https://huggingface.co/nomic-ai/nomic-embed-text-v1.5):
  A. Split texts by semantic chunks to get 1-3 sentences about same subject
  B. Use search_document with terms to filter resulting semantic chunks and keep only those about identity
  C. Embed texts
  D. Cluster using k-means to group texts by theme, examine and evaluate results
     Current progress:
     <img width="1006" height="867" alt="Screenshot 2026-04-15 at 1 07 28 PM" src="https://github.com/user-attachments/assets/03d71ce6-57db-4c9a-9f67-05b0bebddcea" />

  E. Use TF-IDF to get words from all the text in a cluster that "summarize" that cluster
5. Average the text clusters to summarize artists based on their text clustering and embeddings, format to plot on the UI (**_In progress_**)
6. Manually examine clusters and labels to get final cluster labels that will display on UI (**Not yet started**)
7. Visually plot clusters and breakdown of themes over time per artists - see prototype [here](https://mnav0.github.io/thesis/) (**_In progress_**)
  ** Note: right now I'm plotting all of the exported clusters with different values for _n_, this is more exploratory for me to visually understand the results but the final visualization will likely have a couple of versions of these clusters that are combined with the different sources to get a sense of different label/term associations possible with different number of groupings (see below for current progress)
   <img width="1535" height="744" alt="Screenshot 2026-04-15 at 1 08 15 PM" src="https://github.com/user-attachments/assets/6483e775-e911-49a2-a563-30d7ecb0b2ea" />
  <img width="1539" height="813" alt="Screenshot 2026-04-15 at 1 07 59 PM" src="https://github.com/user-attachments/assets/37dc631b-2c16-4fa1-a368-22fb5a936068" />


