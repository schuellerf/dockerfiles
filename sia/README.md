# Sia daemon image

An image containing the sia daemon and client.

## Usage

To start the sia daemon:

    docker run -d --name=siad -v $(pwd)/sia-data:/sia -p 9981:9981 -p 9982:9982 markusk/sia

Then start a shell from within the container and do anything you like:

    docker exec -ti siad bash
    $ siac wallet
