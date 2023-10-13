# Youtube Video Summarizer

**Level**: Advanced

**Target Audience**: Developers / Students

**Prerequisites**: Youtube Transcript API, Python, Supabase

## Description
In this app, the user should be able to upload a youtube video link. Then by loading the transcript file of the video to a knowledge base which in this case will be the supabase vector store, the user should be returned a summary or insights of the video. 
Works best for long podcasts and discussions.
Future enhancement, extracting codes, powerpoint info from the youtube video. The user should also be allowed to ask questions and get results from the video knowledge base.

How does this work?
- First the video transcript/subtitle file is consumed and parsed for removing unnecessary info.
- Then the different parts of the video is truncated into separate blocks.
- Theses blocks are stored in vector database along with their enbeddings.
- Now, when the LLM API from OpenAI or hugging face can be used to summarize the extracted documents and create a summarized article.
- For answering user question backed by video, we perform semantic search for the user query on database.
- Top results from semantic search is attached with the user question, and sent to LLM models which formulates the answer based the provided data.
- This result is then returnable to the user.

## User Stories

- [ ] User can upload youtube link
- [ ] User can get the summarized insights
- [ ] User can ask question against the uploaded video

## Bonus Features

- [ ] User can extract texts, and codes from video using OCR



## Useful Links and Resources
- Supabase https://supabase.com/vector
- https://pypi.org/project/youtube-transcript-api/
- https://www.npmjs.com/package/youtube-transcript
- OpenAI https://platform.openai.com/docs/guides/embeddings

## Example Projects

