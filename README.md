# Capstone: Do lyric embeddings sing a certain song?

## Summary

I propose a natural language processing capstone project using lyrical count vectors from the MusixMatch subset of the Million Song Dataset (MSD).

The goal is to identify the genre, relying on the work by the further expansion from Tagtraum Genre Annotations.

## Project Proposal

### What is the business problem? Who is the stakeholder? Who would benefit?

* Being able to identify genre of a song from its lyrics will allow stakeholders such as playlist creators, music industry professionals, as well as music aficionados a solution to the issue of not being able to identify genre of a song. Having this information will allow for better routing/recommendation of songs for sites.

### What is your data? (Link, EDA in notebook)

* Source of the data:
  * The Million Song Dataset is a freely-available collection of audio features and metadata for a million contemporary popular music tracks. The core of the dataset is the feature analysis and metadata for one million songs, provided by The Echo Nest. Its purposes are:

    * To encourage research on algorithms that scale to commercial sizes
    * To provide a reference dataset for evaluating research
    * As a shortcut alternative to creating a large dataset with APIs
    * To help new researchers get started in the MIR field

  * The musiXmatch dataset (MXM) provides lyrics for many MSD tracks. The lyrics come in bag-of-words format: each track is described as the word-counts for a dictionary of the top 5,000 words across the set. There are 210,519 training bag-of-words, 27,143 testing ones, as well as the full list of words with total counts across all tracks to measure the relative importance of the top 5,000.
* What it describes: Each row in the data describes a song, based on the `track_id`.
* Shape of the data: it is rather large and may need to be stored in a database.
* Initial assessment:
  * Great opportunities for data cleaning & feature engineering
  * Also will need some data preparation and wrangling
  * Possibility to extend dataset to include songs from after the dataset was produced in 2011 to modern day

### What are your criteria for successful minimum viable product?  How will you know if your project succeeded or failed?

* I want to have a classification model selected and tuned for accuracy on the provided training and testing MXM dataset split
* I hope to deploy this to Streamlit or Gradio so others can input lyrics and see what genres it predicts (e.g. "the model thinks this is genre A, but it may also be genre B or genre C")

### What challenges do you foresee?

* Wrangling all this data in different formats and sources and possibly adding to that set is going to be a challenge. It will certainly take a toll on my laptop memory so I may need to use cloud computing to get this going. I have a stretch goal of cleaning the data and having it available for others to use on Kaggle or HuggingFace.
