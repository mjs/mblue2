# mblue2

This is my personal Linux image based on improved [Fedora Silverblue](https://fedoraproject.org/silverblue/) images produced by the [Universal Blue project](https://universal-blue.org/). It began from Universal Blue's [startingpoint template repo](https://github.com/ublue-os/startingpoint) and is occasionally rebased onto that to pick up improvements from the main project.

The major differences from the startingpoint image are:

- Both NVIDIA and non-NVIDIA GPUs images are produced. Some of my machines have NVIDIA GPUs and others don't, so I want to have images for both. My laptops with NVIDIA GPUs also have Intel graphics hardware and they use much less power when the NVIDIA hardware isn't in use so I typically run them with the non-NVIDIA image most of the time. Using an image based distribution makes it trivial to switch between the NVIDIA and standard images. Both image variants share the same packages and configuration - the only difference is the support for NVIDIA hardware.
- A few useful tools are installed into the image like `htop`, `powertop` and `docker-compose`. For desktop applications I almost exclusively use Flatpak, and my command line userspace is a [Distrobox](https://github.com/89luca89/distrobox) container running [Arch Linux](https://archlinux.org/).
- New images with the latest updates are produced every 3 days instead of every day. I don't reboot my machines often enough to justify the electricity required to produce images every day.

On a system that's already running some Universal Blue derived image, this image can be in installed with:

```
rpm-ostree rebase ostree-image-signed:docker://ghcr.io/mjs/mblue2:latest
```

See the [Universal Blue documentation](https://universal-blue.org/) for more information.
