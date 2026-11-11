# Third-party notices

DeepParallax is released under the MIT licence (see [LICENSE](LICENSE)). It relies on the work of
others, listed below. Thank you to all of them.

There are three different situations, and the licence obligations differ for each:

| Component | How DeepParallax uses it | Licence |
|---|---|---|
| mp4-muxer 5.2.2 | **Included** inside `DeepParallax.html` | MIT |
| ONNX Runtime Web 1.17.3 (JavaScript part) | **Included** inside `DeepParallax.html` | MIT |
| ONNX Runtime Web 1.17.3 (engine file `ort-wasm-simd.wasm`) | **Downloaded** when first needed, from jsDelivr | MIT (plus its own third-party notices) |
| Transformers.js 3.8.1 | **Downloaded** when first needed, from jsDelivr | Apache 2.0 |
| Depth Anything V2 Small (the "Standard" AI model) | **Downloaded** when first needed, from Hugging Face | Apache 2.0 |
| Depth Anything V2 Base (the optional "Detailed" AI model) | **Downloaded** only if chosen, from Hugging Face | **CC BY-NC 4.0 — non-commercial use only** |

Nothing in the "Downloaded" rows is stored in this repository. Those files come straight from their
publishers' servers to your browser, under their publishers' terms.

---

## Important: the "Detailed" AI model is for non-commercial use only

Depth Anything V2 comes in several sizes, under different licences. The Small model (used by the
app's **Standard** setting, which is the default) is under the Apache 2.0 licence, which allows
commercial use. The Base model (used only if you choose **Detailed** in the Depth tab) is under the
Creative Commons Attribution-NonCommercial 4.0 licence (CC BY-NC 4.0). That means **videos you make
with the Detailed setting should not be used commercially.** If you plan to sell, license or use your
videos in paid work, keep the AI model on **Standard**.

Source of these terms: the licence section of the Depth Anything V2 project,
<https://github.com/DepthAnything/Depth-Anything-V2>. I am not a lawyer, and this is a summary, not
legal advice. Read the licences themselves if it matters to you.

---

## mp4-muxer 5.2.2

Packs the encoded video into an `.mp4` file. Included in `DeepParallax.html`.
Project: <https://github.com/Vanilagy/mp4-muxer>

```
MIT License

Copyright (c) 2023 Vanilagy

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## ONNX Runtime Web 1.17.3

Runs the depth AI on the main processor when the newer Transformers.js toolkit can't load
(for example in Edge on iPhone and iPad). The JavaScript part (`ort.wasm.min.js`) is included in
`DeepParallax.html`. The engine file (`ort-wasm-simd.wasm`) is downloaded when first needed, or chosen by
hand by the user.
Project: <https://github.com/microsoft/onnxruntime>

```
MIT License

Copyright (c) Microsoft Corporation

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

ONNX Runtime itself contains code from other open-source projects. Their notices are listed in
Microsoft's file: <https://github.com/microsoft/onnxruntime/blob/main/ThirdPartyNotices.txt>

---

## Transformers.js 3.8.1

The main AI toolkit. It downloads and runs the depth model, using the graphics chip (WebGPU) when it
can. Not included in this repository; loaded from
`https://cdn.jsdelivr.net/npm/@huggingface/transformers@3.8.1` when the depth map is first made.
Project: <https://github.com/huggingface/transformers.js>
Licence: Apache License 2.0, <https://www.apache.org/licenses/LICENSE-2.0>
Copyright: Hugging Face, Inc. and contributors.

---

## Depth Anything V2 (AI models)

The AI that estimates how near or far each part of a photo is. DeepParallax uses the ONNX
conversions published by the onnx-community organisation on Hugging Face:

- Standard: <https://huggingface.co/onnx-community/depth-anything-v2-small> — **Apache 2.0**
- Detailed: <https://huggingface.co/onnx-community/depth-anything-v2-base> — **CC BY-NC 4.0 (non-commercial)**,
  <https://creativecommons.org/licenses/by-nc/4.0/>

Original research and models by Lihe Yang, Bingyi Kang, Zilong Huang, Zhen Zhao, Xiaogang Xu,
Jiashi Feng and Hengshuang Zhao. Project: <https://github.com/DepthAnything/Depth-Anything-V2>

If you write about work made with DeepParallax in an academic setting, the authors ask that you cite:

```bibtex
@article{depth_anything_v2,
  title={Depth Anything V2},
  author={Yang, Lihe and Kang, Bingyi and Huang, Zilong and Zhao, Zhen and Xu, Xiaogang and Feng, Jiashi and Zhao, Hengshuang},
  journal={arXiv:2406.09414},
  year={2024}
}
```

---

## Download services

- **jsDelivr** (<https://www.jsdelivr.com>) delivers Transformers.js and the ONNX Runtime engine file.
- **Hugging Face** (<https://huggingface.co>) delivers the AI models.

These services see a normal download request from your browser (as any website does). They never
receive your photos. See [PRIVACY.md](PRIVACY.md).

---

## Trademarks and inspiration

DeepParallax was inspired by **PhotoAwake 3D** (sold by FxFactory for Final Cut Pro) and the free
**Deep Pan** plug-in by **omotion**. DeepParallax is an independent project. It is not affiliated
with, endorsed by or connected to FxFactory, Noise Industries, omotion, Century Creatives or Apple,
and contains none of their code. Final Cut Pro, Safari, iPhone, iPad and Mac are trademarks of Apple
Inc. Microsoft Edge is a trademark of Microsoft Corporation. Other names belong to their owners.

All icons and the sample scene in DeepParallax were drawn for this project.
