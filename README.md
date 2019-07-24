# HIPs 
HyperGAN Improvement Proposals (HIPs) describe standards for the HyperGAN platform, including core functionality, client APIs, and standardized file formats.

# Contributing

 1. Review [HIP-1](HIPs/hip-1.md).
 2. Fork the repository by clicking "Fork" in the top right.
 3. Add your HIP to your fork of the repository. There is a [template HIP here](hip-template.md).
 4. Submit a Pull Request to HyperGAN's [HIPs repository](https://github.com/HyperGAN/HIPs).

Your first PR should be a first draft of the final HIP.  An editor will manually review the first PR for a new HIP before merging it.  Discussions will happen on the pull request.

If your HIP requires images, the image files should be included in a subdirectory of the `assets` folder for that HIP as follows: `assets/hip-N` (where **N** is to be replaced with the HIP number). When linking to an image in the HIP, use relative links such as `../assets/hip-1/image.png`.

When you believe your HIP is mature and ready to progress past the draft phase, you should do one of two things:

 - Open a PR changing the state of your HIP to 'Accepted' or 'Implemented' with a pull request link. An editor will review your draft and ask if anyone objects to its being finalised. If the editor decides there is no rough consensus - for instance, because contributors point out significant issues with the HIP - they may close the PR and request that you fix the issues in the draft before trying again.

# HIP Status Terms

* **Draft** - a HIP that is undergoing rapid iteration and changes.
* **Accepted** - The changes have been accepted as part of the HyperGAN roadmap.
* **Implemented** - The changes have been intergrated in HyperGAN and are ready for release.
* **Released** - The changes are released in the latest HyperGAN library.
