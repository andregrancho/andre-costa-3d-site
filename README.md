# André Costa · 3D personal website

**Live site:** https://andregranchocosta.com

My personal website, built as a walk through a 3D model of my own room. Scrolling moves the camera from object to object. Each stop tells one part of my story: surfing, music and art, basketball, my work at Stats Perform and Endiprev (remote commissioning of offshore wind farms with GE Haliade-X turbines), and what I'm learning in data and AI.

At the end the camera goes out through the window and flies over Farol da Barra (Aveiro, Portugal) at sunset. That's where the CV and contacts are.

## How it was made

| Step | Tools |
|---|---|
| Room modelled and lit in Blender, almost entirely through Python scripts (`bpy`) | Blender 5.3, Python |
| Camera path with 8 stops, exported as keyframes (`percurso.json`) | Blender, Python |
| Barra lighthouse, beach, breakwaters and buildings built from OpenStreetMap data, then rendered as video | OpenStreetMap, Python, Blender (EEVEE), ffmpeg |
| Room exported as glTF with quantised geometry and compressed textures | glTF, Python |
| Website: scroll-driven camera, animated monitor screens, a water shader over the final video loop, mobile layout | three.js, HTML/CSS/JavaScript |

## Structure

```
index.html          the whole site (HTML, CSS, JS)
percurso.json       camera path, stops and light settings exported from Blender
manifest.json       list of model parts
quarto.part*.txt    the room model (.glb split into parts)
v/                  Barra flyover video, seamless final loop, water masks
cv/                 CV (PDF)
```

## Credits

- "Guitarra Gibson acústica" by CastroArbell, "Guitarra Giannini Sunburst" by pinhead19920604, "Cadeira Gamer" by mateusaraujoon (Sketchfab, CC BY 4.0)
- Turntable by thehuntlemod / Dmitriy Isaev (Sketchfab)
- Ukulele by yancharkin (itch.io, CC BY-SA 4.0)
- Textures and plant from Poly Haven (CC0)
- Map data © OpenStreetMap contributors (ODbL)

## License

© André Costa. All rights reserved: the code, the 3D scene, the renders and the artwork in the frames may not be reused without permission. Third-party assets keep their own licences, listed above.
