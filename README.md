Pexels API Python
-------------------------

This Python API wrapper provides easy access to the Pexels API, allowing you to search and retrieve high-quality photos and videos for your projects.

Features
--------

-   Search for photos and videos
-   Access curated and popular content
-   Retrieve specific photos and videos by ID
-   Explore featured collections
-   Manage your personal collections

Installation
------------

bash

`pip install pexels-api-wrapper `

Usage
-----

python

`from pexels_api import PexelsAPI   # Initialize the API with your API key  api = PexelsAPI("YOUR_API_KEY")    # Search for photos  photos = api.search_photos({"query":  "nature",  "per_page":  10})    # Get curated photos  curated = api.curated_photos({"per_page":  15})    # Search for videos  videos = api.search_videos({"query":  "ocean",  "per_page":  5})    # Get popular videos  popular_videos = api.get_popular_videos({"per_page":  20})    # Get featured collections  collections = api.get_featured_collections({"per_page":  10})  `

Available Methods
-----------------

Photos
------

-   `search_photos(params)`: Search for photos
-   `curated_photos(params)`: Get curated photos
-   `get_photos(id)`: Retrieve a specific photo by ID

Videos
------

-   `search_videos(params)`: Search for videos
-   `get_popular_videos(params)`: Get popular videos
-   `get_video(id)`: Retrieve a specific video by ID

Collections
-----------

-   `get_featured_collections(params)`: Get featured collections
-   `get_my_collections(params)`: Get your personal collections
-   `get_collection_media(params)`: Get media from a specific collection

Parameters
----------

Most methods accept a dictionary of parameters. Common parameters include:

-   `query`: Search query (required for search methods)
-   `page`: Page number (default: 1)
-   `per_page`: Results per page (default: 15, max: 80)
-   `orientation`: Photo/video orientation (landscape, portrait, square)
-   `size`: Minimum size (large, medium, small)
-   `locale`: Search locale (e.g., 'en-US', 'fr-FR')

Response
--------

The API returns JSON responses containing relevant data such as:

-   Arrays of Photo or Video objects
-   Pagination information
-   Total results
-   Next/previous page URLs

Error Handling
--------------

The API wrapper includes basic error handling for invalid parameters and API responses. Always check the returned data for any error messages or unexpected results.

Guidelines
----------

Please adhere to the [Pexels API Guidelines](https://www.pexels.com/api/documentation/#guidelines) when using this wrapper and the content provided by Pexels.

