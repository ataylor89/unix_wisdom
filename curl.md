# curl

## What's curl?

Curl is a Unix utility that lets us download a file on the internet. Depending on the options we use, we can eihter print the file to standard output, or save the file to our hard drive.

## What's an example?

Let's say we want to download a CSS file for the dataTables framework. 

> https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.css

We can download the file with a curl command:

    curl https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.css

This prints the file to standard output.

We can save the file to our current directory with the command:

    curl https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.css -o dataTables.bootstrap4.css

The -o option (also --output) is followed by a filename. The -o option tells curl to write the output to the specified file.

But let's say we want the filename to be identical to the remote file name, as in the example above. Why should we type every letter of the file name? 

We can save time with the -O option (uppercase o).

    curl -O https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.css

The -O option tells curl to use the remote filename (dataTables.bootstrap4.css) as the output filename.

So we have discussed three examples of using curl.

    curl https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.css
    curl https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.css -o dataTables.bootstrap4.css
    curl -O https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.css

The first example prints the file to standard output. The second example writes the output to the specified file. The third example writes the output to file and uses the remote filename as the output filename.