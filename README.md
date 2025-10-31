# Content-Based Image Retrieval Using Machine Learning

An intelligent image retrieval system that leverages machine learning techniques to find visually similar images from a large dataset. This MATLAB-based implementation provides efficient content-based image search capabilities using advanced feature extraction and matching algorithms.

## Overview
This application helps researchers, digital asset managers, and computer vision enthusiasts to quickly search and retrieve images based on visual content rather than text-based metadata. Built with a comprehensive feature extraction pipeline and efficient matching algorithms.

## Key Features
- **Interactive GUI**: User-friendly MATLAB interface for image retrieval operations
- **Multi-category Support**: Handles diverse image categories including landscapes, objects, and scenes
- **Feature Extraction**: Advanced Bag of Features (BoF) extraction for robust image representation
- **Efficient Retrieval**: Fast matching algorithm for quick similar image retrieval
- **Extensible Dataset**: Easy integration of new image categories and training data
- **Visual Results**: Clear display of query results with similarity metrics
- **Modular Design**: Well-structured codebase for easy maintenance and extensions

## Architecture
<pre>
```text
           ┌────────────┐
           │    User    │
           │  Interface │
           └─────┬──────┘
                 │
                 ▼
         ┌───────────────────┐        ┌───────────────┐
         │  Image Processing │───────▶│ Feature       │
         │     Pipeline     │        │ Extraction    │
         └────────┬──────────┘        └───────┬───────┘
                  │                           │
                  ▼                           ▼
         ┌────────────────────┐        ┌──────────────────┐
         │  Training Module   │◄───────┤ Bag of Features  │
         │                    │        │    Generator      │
         └────────┬───────────┘        └──────────────────┘
                  │
                  ▼
         ┌────────────────────┐        ┌────────────────┐
         │  Image Database    │◄───────┤  Similarity    │
         │    Management      │        │   Matching     │
         └────────────────────┘        └────────────────┘
```
</pre>

## Project Structure
```
├── cbir_engine/          # Core CBIR implementation files
│   ├── Main_Toolbox.m    # Main application interface
│   ├── readDatabase.m    # Database reading functionality
│   ├── trainDataset.m    # Dataset training implementation
│   ├── selectQuery.m     # Query image selection
│   ├── queryRetrival.m   # Image retrieval implementation
│   └── databaseDisplay01.m # Database display utilities
├── data/                 # Data files and dependencies
│   ├── cbirImageSet.mat  # MATLAB data file for image set
│   └── various .p files  # Compiled MATLAB files
└── Training_set/         # Image dataset categories
    ├── beaches/          # Natural scenes
    ├── bus/             # Transportation
    ├── dinosaurs/       # Historical
    ├── elephants/       # Wildlife
    ├── flowers/         # Nature
    ├── foods/           # Cuisine
    ├── horses/          # Animals
    ├── monuments/       # Architecture
    ├── mountains_and_snow/ # Landscapes
    └── peolpe_in_Africa/  # Cultural
```

## Getting Started

### Prerequisites
- MATLAB R2020a or later
- Image Processing Toolbox
- Computer Vision Toolbox
- 2GB+ free disk space (for image database)

### Installation
1. **Clone the Repository**
```bash
git clone https://github.com/SpoorthyNagendra/Content-Based-Image-Retrieval-Using-Machine-Learning.git
cd Content-Based-Image-Retrieval-Using-Machine-Learning
```

2. **Set Up MATLAB**
- Ensure all required toolboxes are installed
- Add project directory to MATLAB path

3. **Run the Application**
- Navigate to `cbir_engine` directory in MATLAB
- Run `Main_Toolbox.m`

## Usage

### Basic Operations
1. **Read Training Set**
   - Loads and processes images from the dataset
   - Creates necessary data structures for feature extraction

2. **Extract Features**
   - Generates Bag of Features representations
   - Builds feature database for matching

3. **Query Operations**
   - Select query image from file system
   - View similar images retrieved from database
   - Analyze matching results

### Advanced Usage
- Add new image categories to Training_set directory
- Modify feature extraction parameters in trainDataset.m
- Customize similarity metrics in queryRetrival.m

## Technical Stack
| Component | Technology |
|-----------|------------|
| Platform | MATLAB |
| Image Processing | Image Processing Toolbox |
| Feature Extraction | Bag of Features (BoF) |
| GUI | MATLAB GUIDE |
| Database | MAT-files |
| Image Analysis | Computer Vision Toolbox |

## Use Cases
- **Digital Libraries**: Organize and search large image collections
- **Research**: Study image retrieval algorithms and performance
- **Education**: Demonstrate CBIR concepts and implementation
- **Content Management**: Manage and retrieve visual assets
- **Pattern Recognition**: Study feature extraction and matching

## Known Limitations
- Processing time increases with database size
- Limited to image-based queries (no text queries)
- Requires MATLAB and specific toolboxes
- Memory intensive for large image collections
- Feature extraction can be time-consuming for new datasets

## Future Enhancements
- Deep learning-based feature extraction
- Multi-modal query support (text + image)
- Performance optimization for large datasets
- Real-time image retrieval capabilities
- Web-based user interface
- Support for more image formats
- Parallel processing implementation

## Dataset Information
The Training_set directory includes diverse image categories:
- Beaches (Natural scenes)
- Buses (Transportation)
- Dinosaurs (Historical)
- Elephants (Wildlife)
- Flowers (Nature)
- Foods (Cuisine)
- Horses (Animals)
- Monuments (Architecture)
- Mountains and Snow (Landscapes)
- People in Africa (Cultural)

## Contributing
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Team and Roles

This project was developed as part of an undergraduate team project with 4 members:

- **Spoorthy Nagendra** - *Machine Learning Implementation*
  - Implemented the feature extraction algorithms using MATLAB
  - Worked on the Bag of Features (BoF) implementation
  - Contributed to system testing and documentation
  - Collaborated with team members on integration and debugging

- **Team Member 2** - *Database Management & Testing*
- **Team Member 3** - *UI/UX Development*
- **Team Member 4** - *Dataset Curation & Validation*

## Contact
- Email: spoorthynagendra@gmail.com
- LinkedIn: [Spoorthy Nagendra](https://linkedin.com/in/spoorthy-nagendra-ds)

## Acknowledgments
- MATLAB community for toolbox support
- Our project advisor for guidance
- Image dataset providers
- Research papers in CBIR field
- Fellow team members for their valuable contributions

**Note**: This tool is intended for research and educational purposes. Performance may vary based on hardware capabilities and dataset characteristics.