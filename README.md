# cenditel.multimediaplayertheme

## Overview

`cenditel.multimediaplayertheme` is a Plone add-on that provides a theme specifically designed for HTML5 audio and video players within Cenditel multimedia products. It enhances the multimedia experience by incorporating accessible, customizable, and feature-rich media elements into your Plone sites.

## Features

- Custom HTML5 audio and video player themes.
- Accessible player controls and elements.
- Integration with jQuery UI for advanced interactions.
- Support for full window video playback.
- Track captions and audio descriptions.
- Customizable media player controls and behaviors through JavaScript.

## Installation Instructions

### Prerequisites

- Python 2.7
- Plone 4.x
- Buildout

### Steps

1. **Clone the repository:**

    ```sh
    git clone https://github.com/YOUR_USERNAME/cenditel.multimediaplayertheme.git
    cd cenditel.multimediaplayertheme
    ```

2. **Buildout configuration:**

    Add the `cenditel.multimediaplayertheme` to your buildout configuration:

    ```ini
    [buildout]
    extends =
        ...

    ...

    eggs =
        ...
        cenditel.multimediaplayertheme
    ```

3. **Run buildout:**

    ```sh
    ./bin/buildout
    ```

4. **Restart your Plone instance.**

5. **Install the add-on:**

    - Go to the Add-ons control panel.
    - Install the `cenditel.multimediaplayertheme`.

## Usage Examples

### Basic Usage

After installation, the custom multimedia theme will automatically be applied to HTML5 audio and video elements within your Plone site.

### Example Code Snippet

In your Plone site, you can add an HTML5 video element like this:

```html
<video controls>
  <source src="movie.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

This video player will now incorporate the custom theme provided by the `cenditel.multimediaplayertheme`.

## Code Summary

### Code Structure

- **`setup.py`**: Package setup script. Defines the package metadata and dependencies.
- **`cenditel/__init__.py`**: Package namespace declaration.
- **`cenditel/multimediaplayertheme/setuphandlers.py`**: Setup handlers for import steps during installation.
- **`cenditel/multimediaplayertheme/tests.py`**: Unit tests configuration and setup for Plone integration.
- **`cenditel/multimediaplayertheme/__init__.py`**: Initializer for Zope 2 product.
- **`cenditel/multimediaplayertheme/browser/interfaces.py`**: Browser layer interface for the theme.
- **`cenditel/multimediaplayertheme/browser/viewlets.py`**: Definition of viewlets for the theme.
- Various **JavaScript files** under `cenditel/multimediaplayertheme/browser/javascripts/` for enhanced media player functionalities and custom interactions.

### Key Files

- `jme-debug.js`: Debugging utility for jMediaElement projects.
- `jmeEmbedControls.js`: Adds predefined control markup for rapid development with jME.
- `a11y-slider.ext.js`: Extends jQuery UI's slider with accessibility features.
- `enterLeave.js`: Alternative to hover with more accessibility.
- `fullwindow.js`: Enables full window video playback.
- `timerange.js`: Adds timing ranges for media events.
- `track.js`: Plugin for handling subtitles and audio descriptions.

## Contributing Guidelines

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-name`).
6. Create a new Pull Request.

Ensure your code follows the project's coding standards and includes tests where applicable.

## License

This project is licensed under the MIT license. See the `LICENSE` file for details.
