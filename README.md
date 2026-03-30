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

An initial sampling of data collected is available [here](https://github.com/PSAM-5020/Project/tree/main/data).

### Process outline
1. Collect data - public artist statements, interviews, artwork titles, and institutional biographical text will be the data considered for the analysis
2. Run classification models to extract themes from blocks of text (potentially [nomic-embed-text-v1.5](https://huggingface.co/nomic-ai/nomic-embed-text-v1.5) or [mixedbread-ai/mxbai-embed-large-v1](https://huggingface.co/mixedbread-ai/mxbai-embed-large-v1))
3. Grade each artist by theme based on the level that their words are classified to one theme vs. others (some of the models may already do this step or output clusters, the approach to steps 3 and 4 depends on what models are used)
4. Use k-means clustering to group artists by themes typically explored in their work
5. Visually plot clusters and breakdown of themes over time per artists - see prototype [here](https://mnav0.github.io/thesis/)
