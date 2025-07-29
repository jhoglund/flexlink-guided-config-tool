# FlexLink Configuration Tool

A comprehensive tool for extracting FlexLink component specifications from catalogs and building guided configuration systems.

## 🏗️ Project Structure

```
flexlink-tool/
├── data/                          # Extracted component data
│   ├── large_catalog_extraction/  # Main catalog extraction results
│   └── enhanced_components.json   # Components with application info
├── web/                           # Current web interface
│   └── index.html                 # Component viewer
├── scripts/                       # Python extraction scripts
│   ├── component_extractor.py     # Core component extractor
│   ├── enhanced_component_extractor.py  # Enhanced with application info
│   ├── extract_large_catalog_offline.py # Large catalog processor
│   └── upload_to_database.py     # Database uploader
├── database/                      # Database schema and migrations
│   ├── database_schema.sql        # Main database schema
│   └── update_database_schema.sql # Application fields schema
└── docs/                          # Documentation
    ├── README_COMPONENT_EXTRACTION.md
    └── USAGE_GUIDE.md
```

## 🚀 Current Status

✅ **Completed:**
- 603 components extracted from FlexLink catalog
- All components uploaded to Supabase database
- Basic web interface for component viewing
- Resilient upload system with progress tracking

🔄 **In Progress:**
- Enhanced extraction with application information
- System-level intro text extraction
- Application filtering capabilities

🎯 **Next:**
- Rails-based guided configuration tool
- Step-by-step wizard interface
- 3D visualization and optimization

## 📊 Data Overview

**Extracted Components:**
- **603 total components** from 500+ page catalog
- **102 XH components** (hygienic system)
- **Multiple system types:** X45, XS, X65, X85, X180, X300, XH, XK
- **Component types:** Chains, Sprockets, Bearings, Tracks, Drive Units, Bends

**Database Schema:**
- `component_specifications` table in Supabase
- JSONB fields for flexible specifications
- Application flags for filtering
- Full text search capabilities

## 🛠️ Technology Stack

**Current:**
- **Python** - Data extraction and processing
- **Supabase** - PostgreSQL database
- **HTML/CSS/JavaScript** - Web interface
- **PyMuPDF/pdfplumber** - PDF processing

**Planned:**
- **Ruby on Rails** - Guided configuration tool
- **PostgreSQL** - Component database
- **React/Vue.js** - Frontend wizard interface
- **Three.js** - 3D visualization

## 🔧 Setup Instructions

### 1. Environment Setup
```bash
# Clone repository
git clone <your-repo-url>
cd flexlink-tool

# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Database Setup
```bash
# Set up Supabase credentials in .env file
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_key

# Run database schema
# Copy database_schema.sql to Supabase SQL Editor and execute
```

### 3. Extract Components
```bash
# Extract from catalog
python extract_large_catalog_offline.py "path/to/catalog.pdf"

# Upload to database
python upload_to_database.py --batch-size 10
```

## 🎯 Guided Configuration Tool (Planned)

The Rails application will provide:

### Step 1: Challenge Definition
- Extending existing line
- New production line
- Replacing equipment

### Step 2: Environmental Requirements
- Cleanroom
- Washdown
- Standard
- ESD-safe

### Step 3: Solution Complexity
- Simple extension
- Custom configuration
- Complete system

### Step 4: Progressive Configuration
- Component selection based on requirements
- Automatic compatibility checking
- Cost optimization

### Step 5: 3D Visualization
- Interactive 3D model
- Optimization suggestions
- Export capabilities

## 📈 Application Filtering

Filter components by:
- **Washable** - Hygienic systems (XH)
- **Food Grade** - FDA approved components
- **Heavy Duty** - Industrial systems (X65, X85, X180, X300)
- **Chemical Resistant** - Corrosive environments (XK)
- **High Temperature** - Heat resistant applications

## 🔄 Resume Capability

All extraction and upload processes support:
- **Progress tracking** - Resume from interruptions
- **Batch processing** - Handle large catalogs
- **Error recovery** - Retry failed operations
- **Data persistence** - Local backup of all results

## 📝 Development Notes

**Current Data:**
- 603 components in Supabase
- All specifications and dimensions captured
- System codes and compatibility mapped
- Ready for Rails integration

**Next Steps:**
1. Set up Rails application
2. Connect to Supabase database
3. Build wizard interface
4. Implement 3D visualization
5. Add optimization algorithms

## 🤝 Contributing

1. Fork the repository
2. Create feature branch
3. Make changes
4. Test thoroughly
5. Submit pull request

## 📄 License

[Your License Here]

---

**Last Updated:** July 29, 2024  
**Status:** ✅ Core extraction complete, 🚧 Rails development pending 