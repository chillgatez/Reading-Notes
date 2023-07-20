# Class03 Readings: File Manipulation / System.IO

- File and stream I/O (input/output) play a crucial role in data transfer to or from a storage medium in .NET. The System.IO namespaces provide various types that facilitate reading and writing data streams and files, both synchronously and asynchronously. These namespaces also include classes for compression, communication through pipes and serial ports, and isolated storage.  

- When dealing with files, you work with ordered collections of bytes stored persistently, along with directory paths and names. In contrast, streams are sequences of bytes that can be read from and written to various backing stores, such as disks, memory, or networks. The System.IO namespace offers several classes for interacting with files and directories, like File, FileInfo, Directory, and DirectoryInfo, as well as methods for processing directory strings in a cross-platform manner with Path.  

- In the realm of streams, the abstract base class Stream and its derived classes enable reading, writing, and seeking within a stream. Depending on the specific data source, a stream may support only certain operations. Some commonly used stream classes include FileStream, IsolatedStorageFileStream, MemoryStream, BufferedStream, NetworkStream, PipeStream, and CryptoStream. Additionally, reader and writer classes handle the conversion of encoded characters to and from bytes, allowing interaction with streams as byte input and output. Some frequently used reader and writer classes are BinaryReader, BinaryWriter, StreamReader, StreamWriter, StringReader, StringWriter, TextReader, and TextWriter.  

- Asynchronous I/O operations are recommended when dealing with resource-intensive data transfer to maintain application responsiveness. In Windows Store apps, certain differences exist, such as using the types in the Windows.Storage namespace instead of System.IO for file operations. Moreover, isolated storage is unavailable for Windows 8.x Store apps, replaced by application data classes. It is essential to consider security requirements, including access control lists (ACLs), when using System.IO classes. Internet and intranet applications should use isolated storage for security purposes and avoid granting access to physical files in less-trusted code or application domains.

## Summary

**_Reading and writing files in .NET can be compared to using a notebook._**
    
- Reading a file is like flipping through the pages of the notebook and getting information from it. You read what others have written in the notebook and gather knowledge from it.

- Writing to a file is like grabbing a pen and jotting down your own thoughts, ideas, or data into the notebook. You contribute your own information to be stored and shared with others.

- Creating a new data file is akin to opening a fresh notebook with empty pages. You start from scratch, creating a space to store new information.

- Just as you can read from and write to different notebooks with various types of content, in .NET, you can use different classes and methods to handle files of different formats and data types.

**_In essence, file manipulation in .NET is all about managing information flow, just like using a notebook for gathering, sharing, and creating new knowledge._**
