<img src="./gigagan-sample.png" width="500px"></img>

<img src="./gigagan-architecture.png" width="500px"></img>

## GigaGAN - Pytorch (wip)

Implementation of <a href="https://arxiv.org/abs/2303.05511">GigaGAN</a> <a href="https://mingukkang.github.io/GigaGAN/">(project page)</a>, new SOTA GAN out of Adobe.

I will also add a few findings from <a href="https://github.com/lucidrains/lightweight-gan">lightweight gan</a>, for faster convergence (skip layer excitation), better stability (reconstruction auxiliary loss in discriminator), as well as improved results (GLU in generator).

It will also contain the code for the 1k - 4k upsamplers, which I find to be the highlight of this paper.

Please join <a href="https://discord.gg/xBPBXfcFHd"><img alt="Join us on Discord" src="https://img.shields.io/discord/823813159592001537?color=5865F2&logo=discord&logoColor=white"></a> if you are interested in helping out with the replication with the <a href="https://laion.ai/">LAION</a> community

## Appreciation

- <a href="https://stability.ai/">StabilityAI</a> for the sponsorship, as well as my other sponsors, for affording me the independence to open source artificial intelligence.

- <a href="https://huggingface.co/">🤗 Huggingface</a> for their accelerate library

- All the maintainers at <a href="https://github.com/mlfoundations/open_clip">OpenClip</a>, for their SOTA open sourced contrastive learning text-image models

## Todo

- [x] make sure it can be trained unconditionally
- [ ] read the relevant papers and knock out all 3 auxiliary losses
    - [x] matching aware loss
    - [x] clip loss
    - [ ] vision-aided adversarial loss
    - [ ] add reconstruction losses on arbitrary stages in the discriminator (lightweight gan)
- [ ] get a code review for the multi-scale inputs and outputs, as the paper was a bit vague
- [ ] port over CLI from lightweight|stylegan2-pytorch
- [ ] hook up laion dataset for text-image

## Citations

```bibtex
@misc{https://doi.org/10.48550/arxiv.2303.05511,
    url     = {https://arxiv.org/abs/2303.05511},
    author  = {Kang, Minguk and Zhu, Jun-Yan and Zhang, Richard and Park, Jaesik and Shechtman, Eli and Paris, Sylvain and Park, Taesung},  
    title   = {Scaling up GANs for Text-to-Image Synthesis},
    publisher = {arXiv},
    year    = {2023},
    copyright = {arXiv.org perpetual, non-exclusive license}
}
```

```bibtex
@article{Liu2021TowardsFA,
    title   = {Towards Faster and Stabilized GAN Training for High-fidelity Few-shot Image Synthesis},
    author  = {Bingchen Liu and Yizhe Zhu and Kunpeng Song and A. Elgammal},
    journal = {ArXiv},
    year    = {2021},
    volume  = {abs/2101.04775}
}
```
