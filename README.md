# eLAB Analytics Dashboard

Interactive analytics dashboard for eLAB veterinary laboratory management system.

## 🎯 Features

- **9 Interactive Charts** - Visualize tests, species, employees, districts, and revenue
- **7 Data Tabs** - Dashboard, Districts, Employees, Tests, Species, Monthly, Yearly
- **Sortable Tables** - Click any column to sort, search, and filter
- **Export to Excel** - Download full reports or individual tables
- **Real-time Data** - All data from Supabase database
- **Responsive Design** - Works on desktop, tablet, and mobile

## 📊 Analytics Included

### Dashboard KPIs
- Total Cases: 5,468
- Total Revenue: ₹3,484,275
- Average Revenue per Case
- Payment Completion Rate
- Sample Collection Rate
- Report Sent Rate
- Unique Customers: 3,168
- Total Employees: 64

### Data Analysis
- **District-wise**: 27 districts analyzed
- **Employee Performance**: 48 employees tracked
- **Test Analysis**: 120 test types
- **Species Breakdown**: 13 species
- **Monthly Trends**: 9 months of data (Mar-Nov 2025)
- **Yearly Summary**: Annual performance metrics

## 🚀 Live Demo

Visit: [Your Vercel URL here after deployment]

## 💻 Local Development

### Prerequisites
- Python 3.8+
- Supabase account

### Installation

1. Clone the repository:
```bash
git clone https://github.com/drshintoantony/elab.git
cd elab
```

2. Install dependencies:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Configure Supabase:
```bash
cp .env.example .env
# Edit .env and add your Supabase credentials
```

4. Generate analytics data:
```bash
python elab_analytics_fixed.py
```

5. Start local server:
```bash
./start_dashboard.sh
```

Visit: http://localhost:8000

## 📁 File Structure

```
elab/
├── index.html                          # Landing page (redirects)
├── elab_analytics_dashboard.html       # Main dashboard
├── elab_analytics_data.json           # Analytics data (977 records)
├── elab_analytics_complete.xlsx       # Full Excel export (985 rows)
├── elab_analytics_fixed.py            # Data export script
├── requirements.txt                   # Python dependencies
├── vercel.json                        # Vercel configuration
├── .env.example                       # Environment template
└── README.md                          # This file
```

## 🔧 Configuration

### Supabase Setup

1. Go to https://app.supabase.com
2. Select your project
3. Navigate to Settings → API
4. Copy:
   - Project URL → SUPABASE_URL
   - service_role key → SUPABASE_KEY

Add these to your `.env` file.

### Vercel Deployment

1. Push to GitHub
2. Import project in Vercel
3. Deploy (no build steps needed - static site)

## 📊 Data Export

### Generate Fresh Data

```bash
source venv/bin/activate
python elab_analytics_fixed.py
```

Options:
- **Option 1**: Export ALL data (no date filter)
- **Option 2**: Export specific time period

This generates:
- `elab_analytics_complete.xlsx` - Full Excel report
- `elab_analytics_data.json` - Dashboard data

## 🎨 Dashboard Features

### Tabs

1. **Dashboard** - Overview with 8 KPIs + 6 charts
2. **Districts** - Geographic analysis with sortable table
3. **Employees** - Performance metrics and test breakdown
4. **Tests** - Test volume, revenue, and trends
5. **Species** - Animal species breakdown
6. **Monthly** - Month-by-month analysis with trends
7. **Yearly** - Annual summary

### Charts

- Top Tests by Volume (bar)
- Species Distribution (doughnut)
- Employee Performance (dual-axis bar)
- Top Districts by Revenue (horizontal bar)
- Monthly Revenue Trend (line)
- Test Category Distribution (bar)
- Species Trends (multi-line)
- Monthly Analysis (line + dual-axis)
- Yearly Analysis (bar + dual-axis)

### Tables

All tables support:
- ✓ Sort by clicking column headers
- ✓ Search/filter functionality
- ✓ Pagination
- ✓ Export to Excel

## 📈 Data Accuracy

- **Revenue Calculation**: Uses `total_test_charge` (excludes collection charges)
- **Records**: 5,468 visits, 17,853 tests
- **Coverage**: All districts, employees, species, and test types
- **Time Period**: March 2025 - November 2025

## 🛠️ Technologies

- **Frontend**: HTML, CSS, JavaScript
- **Charts**: Chart.js
- **Tables**: DataTables
- **Backend**: Python 3
- **Database**: Supabase (PostgreSQL)
- **Hosting**: Vercel
- **Export**: openpyxl, pandas

## 📝 License

Proprietary - eLAB Veterinary Laboratory Management System

## 👤 Author

Dr. Shinto Antony
- GitHub: [@drshintoantony](https://github.com/drshintoantony)

## 🤝 Support

For issues or questions, please open an issue on GitHub.

---

**Last Updated**: November 25, 2025
**Version**: 3.0
