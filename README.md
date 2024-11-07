# File-System-in-C

## Simple File System (SFS) Implementation

This project implements a simple file system (SFS) in C, utilizing block-based storage. The system is designed to manage files and directories using a custom inode structure and block management system.

## Features

- **Block-Based Storage**: The file system is built using fixed-size blocks (1 KB each).
- **Inode-Based File Management**: Each file or directory is represented by an inode, which stores pointers to data blocks.
- **Block Bitmap**: Tracks the usage of data blocks (whether they are free or allocated).
- **Inode Bitmap**: Tracks the allocation status of inodes.
- **Superblock Management**: Contains metadata about the file system, such as the total number of blocks and inodes.

## File Structure

- **`202101255_Proj1_sfs_mysol.c`**: The core implementation of the simple file system.
- **`sfs.disk`**: Disk file used by the file system to simulate block storage.

## How to Run

1. Compile the C program:
    ```bash
    gcc 202101255_Proj1_sfs_mysol.c -o sfs
    ```

2. Run the compiled file with the `sfs.disk` file:
    ```bash
    ./sfs sfs.disk
    ```

## Project Details

- **Inode Structure**: Each inode can point to three data blocks, which store the contents of a file or directory.
- **Block Size**: 1 KB (1024 bytes).
- **Max Blocks**: 100 blocks (from `BLOCK_SUPER` to `BLOCK_MAX`).
- **Max Inodes**: 128 inodes (from `INODE_MAX`).

## Usage

The file system provides basic file management functionalities such as:

- File creation
- File deletion
- Reading from and writing to files
- Directory creation and management
