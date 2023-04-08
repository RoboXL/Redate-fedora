#!/bin/bash

read -p "This script will update your installed packages using DNF. Do you want to proceed? [y/n] " proceed

if [ "$proceed" == "y" ]; then
    # Update package list
    echo "Updating package list..."
    sudo dnf updateinfo

    # Upgrade packages
    echo "Upgrading packages..."
    sudo dnf upgrade --refresh

    # Clean up
    echo "Cleaning up..."
    sudo dnf clean all

    # Ask user if they want to restart
    read -p "Packages have been updated. Do you want to restart your computer now? [y/n] " restart
    if [ "$restart" == "y" ]; then
        sudo shutdown -r now
    fi
else
    echo "Update cancelled."
fi
