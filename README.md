# Camera 3000

A silly little camera webapp.

I'm excited to share my new web app: [**Camera 3000: The Camera of the Future**](https://brianweinstein.github.io/camera-3000/)[^1].

It's an AI-powered camera app that captures everything in the scene *except* the important details, so the photo you get is eerily similar to reality, but not quite right.[^2] It just barely “takes a photo.”

![](/public/camera-3000-carrot.png)


I was loosely inspired by the [“What is a photo?”](https://www.theverge.com/2024/9/23/24252231/lets-compare-apple-google-and-samsungs-definitions-of-a-photo) debate and the rampant [overuse of AI](https://www.fastcompany.com/91154806/ai-in-everything-era-pointless). I'm sure there's something deep to say about both of these, but I have nothing new to add to that discourse. In reality, I just thought it’d be fun to take those ideas to the extreme.

![](/public/camera-3000-bookshelf.png)


**How it works:** Given a photo, the app first uses the Gemini API to generate a detailed description of the image. Next, the Imagen API uses that description as a prompt to create a new, entirely-AI image of something that only sort of resembles the original scene.

**How it's made:** In the spirit of overusing AI, I used Gemini/Canvas[^3] to write most of the app’s [code](https://github.com/BrianWeinstein/real-photo-camera-app/tree/main) and followed its instructions to get the app live. In the spirit of over-overusing AI, I did almost everything it told me to do, too, including things I knew to be terrible, like publicly exposing my API key[^4]. I'm sure there's a lesson here somewhere.[^5]

![](/public/camera-3000-monument.png)


**The app could use some polish:** The error states are wonky, the UI is barebones, and I've given up on allowing a range of aspect ratios for the photo, but alas, it's just a silly little novelty app. It's functional, so just have fun with it.

**Please be kind in your use of this app:** I recognize that image generation can be used for malicious purposes, so the app will [error out](https://cloud.google.com/vertex-ai/generative-ai/docs/multimodal/configure-safety-filters#configurable-filters) if a user attempts to generate harmful images. All of the AI generated images adhere to the [SynthID](https://deepmind.google/science/synthid/) digital watermarking standard too.

[Please go try it out\!](https://brianweinstein.github.io/camera-3000/) The AI-everywhere future is already here, and it’s partially running on a publicly exposed API key.[^6]  

---

[^1]:  It’s the “camera of the future” in the same way that Dippin' Dots is the “ice cream of the future”: it's not, and it's not even good at being the camera / ice cream of the present. For what they are, Camera 3000 and Dippin’ Dots are both incredibly energy inefficient too. The parallels are unparalleled.

[^2]:  This is somehow only the second-dumbest thing I’ve ever created. See my [froyo map](https://bweinstein.medium.com/mapping-the-frozen-yogurt-shop-closest-to-each-manhattan-apartment-3785ccd34f4c) from 2016\. Still ranking \#1 on Google for “froyo map nyc,” despite the map being broken 🎉.

[^3]:  I used Gemini/Canvas. I just learned about [Firebase Studio](https://firebase.google.com/) last week, which would’ve made building this app 1000x easier.

[^4]:  Don’t worry, I put some severe restrictions on the API key’s use. But still, please send your thoughts and prayers that I don’t wake up to a million-dollar GCP bill.

[^5]:  In the spirit of over-over-overusing AI, I tried to use Gemini to write this blog post based on the app’s code, but the generated text was just awful. The number of times I prompted “make this sound less pompous” …

[^6]:  Gemini wrote this closing sentence, though. Kinda funny, but still sounds a bit pompous. I’m sure there’s a lesson here too.
