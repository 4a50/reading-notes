# Notes for Read 03 - System.IO

## File and Stream I/O
[File and Stream I/O](https://docs.microsoft.com/en-us/dotnet/standard/io/)
Transfer of data either to or from a storage medium.

### Commonly used File and directory classes:

+ File - *static* methods to create, copy, delete, moving and opening files
+ FileInfo - *instance* methods for create, copy, delete, moving and opening and helps create a FileStream object.
+ Directory -provides static methods for creating, moving, and enumerating through directories and subfolder.
+ DirectoyInfo - provides instance methods and properties for processing directory strings in a cross-platform manner.

**Streams**
The abstract base class Stream supports reading and writing bytes. 

+ Reading - transferring data from a stream into a data structure, such as an array of bytes.
+ Writing - transferring data to a stream from a data source.
+ Seeking - querying and modifying the current position within a stream.

#### Common Classes:

+ FileStream – for reading and writing to a file.
+ IsolatedStorageFileStream – for reading and writing to a file in isolated storage.
+ MemoryStream – for reading and writing to memory as the backing store.
+ BufferedStream – for improving performance of read and write operations.
+ NetworkStream – for reading and writing over network sockets.
+ PipeStream – for reading and writing over anonymous and named pipes.
+ CryptoStream – for linking data streams to cryptographic transformations.

### Readers and Writers

The System.IO namespace also provides types for reading encoded characters from streams and writing them to streams

#### Common Classes:

+ BinaryReader and BinaryWriter – for reading and writing primitive data types as binary values.
+ StreamReader and StreamWriter – for reading and writing characters by using an encoding value to convert the characters to and from bytes.
+ StringReader and StringWriter – for reading and writing characters to and from strings.
+ TextReader and TextWriter – serve as the abstract base classes for other readers and writers that read and write characters and strings, but not binary data.

### Async I/O Operations


Reading or writing a large amount of data can be resource-intensive. You should perform these tasks asynchronously if your application needs to remain responsive to the user.

### Compression

#### Common Classes

+ ZipArchive – for creating and retrieving entries in the zip archive.
+ ZipArchiveEntry – for representing a compressed file.
+ ZipFile – for creating, extracting, and opening a compressed package.
+ ZipFileExtensions – for creating and extracting entries in a compressed package.
+ DeflateStream – for compressing and decompressing streams using the Deflate algorithm.
+ GZipStream – for compressing and decompressing streams in gzip data format.

## Write to a file
[Writing to a file](https://docs.microsoft.com/en-us/dotnet/standard/io/how-to-write-text-to-a-file)
Example:

From Microsoft Docs

```using System;
using System.IO;

class Program
{
    static void Main(string[] args)
    {

        // Create a string array with the lines of text
        string[] lines = { "First line", "Second line", "Third line" };

        // Set a variable to the Documents path.
        string docPath =
          Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

        // Write the string array to a new file named "WriteLines.txt".
        using (StreamWriter outputFile = new StreamWriter(Path.Combine(docPath, "WriteLines.txt")))
        {
            foreach (string line in lines)
                outputFile.WriteLine(line);
        }
    }
}
```

## Reading to a File
[Reading to a File](https://docs.microsoft.com/en-us/dotnet/standard/io/how-to-read-and-write-to-a-newly-created-data-file)
example:

```using System;
using System.IO;

class MyStream
{
    private const string FILE_NAME = "Test.data";

    public static void Main()
    {
        if (File.Exists(FILE_NAME))
        {
            Console.WriteLine($"{FILE_NAME} already exists!");
            return;
        }

        using (FileStream fs = new FileStream(FILE_NAME, FileMode.CreateNew))
        {
            using (BinaryWriter w = new BinaryWriter(fs))
            {
                for (int i = 0; i < 11; i++)
                {
                    w.Write(i);
                }
            }
        }

        using (FileStream fs = new FileStream(FILE_NAME, FileMode.Open, FileAccess.Read))
        {
            using (BinaryReader r = new BinaryReader(fs))
            {
                for (int i = 0; i < 11; i++)
                {
                    Console.WriteLine(r.ReadInt32());
                }
            }
        }
    }
}
```
[&lt;--&#91;BACK&#93;](/README.md)