# doc-RAG


this is RAG for documents. it accepts all `.docx` , `.pdf` , `.txt` you put in sources folder. just put the data you have in sources folder and it will answer your question with data you gave it. you can put multiple PDFs and txts with different topics at the same time and get you answers about those docs but i suggest to not overdo this.
<br />there are somethings i like to point out:
* i built and tested this using langchain and BGE-M3 for embedding and gemma3 as LLM.
* i used ollama to load models but you can simply import other things like llama.cpp , GPT4ALL ,...
* there are two prompts. one for model to only answer based on docs you gave it and one that allow model to use its base knowledge too beside docs you gave it. you can simply comment the one you dont need and uncomment (if its commented) the one you need.
* if you dont have BGE-M3 locally there is some commented code which download it for you and simply go to your cache folder(in PATH of you env or simply the PATH but im not sure where exactly) and relocate it if you want and use the code written for loading locally. but downloading BGE-M3 is not necessary if you have API key.
* if you have OpenAI API or ... there is a block of code for you to simply use your API key to access embedding and LLM instead of loading locally. just uncomment them and comment those codes written for doing all that locally.

i really suggest running your models with gpu. i ran models with both CPU and GPU. it made 90 sec with i5-12400f to 2 sec with RX 6600 XT!


