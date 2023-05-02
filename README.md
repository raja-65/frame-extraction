# frame-extraction
https://drive.google.com/file/d/1_OtZktBQcTUMlRXa4bnCG-QA-Gf7jEzO/view?usp=share_link       ( go here for folder because i am not able to upload here it is showing large file size)
This is an Android application written in Kotlin that extracts frames from a video file and displays them in a RecyclerView. The application uses a custom decoder to extract frames from the video and saves them as image files. The frames are then displayed in a RecyclerView using an adapter.

The application first requests permissions to read from external storage, as it needs to access the video file. The user can then select a video file from their gallery using the device's default file picker. Once a video file is selected, the application starts extracting frames from the video using a custom decoder. The extracted frames are then saved as image files in the app's external file directory. After all the frames are extracted, the application displays them in a RecyclerView using an adapter.

The RecyclerView is configured to display the images in a staggered grid layout with three columns. The adapter is responsible for loading the images and displaying them in the grid. The adapter also displays the title of the video file along with each frame.

The application uses a custom decoder to extract frames from the video. The decoder is implemented in the FrameExtractor class and implements the IVideoFrameExtractor interface. The decoder extracts frames by iterating through the video frames and saving each frame as an image file. The extracted frames are then passed to the onCurrentFrameExtracted method of the IVideoFrameExtractor interface, where they are converted to Bitmaps and saved as image files. The extraction process is run on a separate thread using an ExecutorService to avoid blocking the main thread.

The application uses several helper classes and functions to perform various tasks. The URIPathHelper class is used to convert a content URI to a file path. The Utils class provides several utility functions, including a function to convert a byte buffer to a Bitmap. The ImageAdapter class is responsible for loading the images and displaying them in the RecyclerView.

The application also displays some information about the extraction process, including the total time it took to extract all frames, in a TextView.
