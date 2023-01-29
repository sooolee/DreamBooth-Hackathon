# DreamBooth Hackathon

I participated in a community event [DreamBooth Hackathon](https://huggingface.co/spaces/dreambooth-hackathon/leaderboard) organized by Hugging Face between Dec. 2022 - Jan 2023. The goal is fine-tuning a Stable Diffusion model with a technique called [DreamBooth](https://dreambooth.github.io/).

My choice of a subject was Rex the Toy Dinosaur from the Toy Story. The dataset ([sooolee/rexthetoy](https://huggingface.co/datasets/sooolee/rexthetoy)) was obtained from the web. Samples from the dataset are presented below.

![dataset](https://github.com/sooolee/dreambooth-hackathon/blob/main/images/dataset.png?raw=true)

I chose version 1.5 of the Stable Diffusion model ([runwayml/stable-diffusion-v1-5](https://huggingface.co/runwayml/stable-diffusion-v1-5)). The model was trained with `a learning rate of 1e-06` and `1000 train steps`.

The trained model is uploaded to the Hugging Face hub. Please visit my repo: [sooolee/rex-the-toy-dinosaur](https://huggingface.co/sooolee/rex-the-toy-dinosaur?text=a+photo+of+rxty+dinosaur+reading+a+book+in+a+cafe)

-------------

## Inference Samples
Here are some examples of inferences (the good ones! :smiley:) made with a guidance scale between 8 - 11 and inference steps of 300 - 400. 

### In Places
`instance_prompt` examples include: 'A photo of rxty dinosaur in Grand Canyon', 'A photo of rxty dinosaur in Paris with Eiffel tower as a background', 'A photo of rxty dinosaur in the Acropolis'.

![in_places](https://github.com/sooolee/dreambooth-hackathon/blob/main/images/in_places.png?raw=true)

### Artistic Rendering
The prompt examples include: '... in the style of Johannes Vermeer', '...in the sytle of Vincent Van Gogh', '...in the style of Michelangelo', '...in the style of Leonardo da Vinci'.

![artistic_rendering](https://github.com/sooolee/dreambooth-hackathon/blob/main/images/artistic_rendering.png?raw=true)

### Doing Things
The prompt examples include: '...reading a book in a cafe', '...playing baseball', '...riding a bike in a city', '...surfing in the ocean', 'swimming in a pond'.

![doing_things](https://github.com/sooolee/dreambooth-hackathon/blob/main/images/doing_things.png?raw=true)


## Afterthoughts

I have to admit that the model is slightly overfitted. And it is somewhat intentional. I had trained the model with the same dataset but with a higher learning rate (1e-5 ~ 2e-6) and less training steps (600 ~ 800). These models made more diverse poses in doing actions but at the same time disfigured Rex the Toy more frequently. I preferred keeping the face and shape of Rex, sacrificing diversity to some degree. I am happy with the outputs of the final model with the 1e-6 learning rate and 1000 training steps. 