# Cowsay

*Cowsay* is a program written in Perl that generates an ASCII picture of a cow saying something provided by the user.

For this project, we're are using fortune, a program written in C, that according to its manpage, prints a rantom, hopefully intersting, adage.

So, the idea is to run:

```bash
$ fortune | bash
```

Everytime that a container is created using this image.

## Build the Image

```bash
docker build . -t cowsay:latest
```

## Run the container

```bash
docker run --rm -it cowsay
```
