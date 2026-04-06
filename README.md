<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>D Go Impact Report | Dimag Ghochne Manche</title>
    <!-- Google Fonts for Professional Look -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    
    <style>
        :root {
            /* Exact Logo Theme Colors */
            --dgo-purple: #8b5cf6;
            --dgo-pink: #d946ef;
            --dgo-red: #f43f5e;
            --dgo-gradient: linear-gradient(90deg, #8b5cf6, #d946ef, #f43f5e);
            
            --bg-light: #fdfdff;
            --text-main: #1e293b;
            --text-muted: #64748b;
            --white: #ffffff;
            --success: #10b981;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #f1f5f9;
            color: var(--text-main);
            margin: 0;
            padding: 20px;
            line-height: 1.6;
        }

        .report-container {
            max-width: 1100px;
            margin: 0 auto;
            background: var(--white);
            border-radius: 20px;
            box-shadow: 0 15px 50px rgba(0,0,0,0.1);
            overflow: hidden;
            border-top: 8px solid transparent;
            /* Applying gradient border effect at the very top */
            border-image: var(--dgo-gradient);
            border-image-slice: 1;
        }

        /* Top Header & Logo Area */
        .branding-header {
            padding: 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: linear-gradient(to bottom, #fafafa, #ffffff);
            border-bottom: 1px solid #edf2f7;
        }

        .logo-placeholder {
            max-width: 180px;
            /* In case image isn't loaded, text will look like branding */
            font-weight: 800;
            font-size: 2rem;
            background: var(--dgo-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .logo-placeholder img {
            width: 100%;
            height: auto;
        }

        .project-badge {
            background: var(--dgo-gradient);
            color: white;
            padding: 8px 18px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Main Content */
        .content { padding: 40px; }

        .headline-section { margin-bottom: 40px; }
        .headline-section h1 { font-size: 2.2rem; margin: 0; color: #0f172a; }
        .headline-section p { color: var(--text-muted); font-size: 1.1rem; margin-top: 5px; }

        /* Summary Cards */
        .summary-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 25px;
            margin-bottom: 50px;
        }

        .card {
            padding: 30px;
            border-radius: 16px;
            background: #f8fafc;
            border: 1px solid #e2e8f0;
            position: relative;
            transition: transform 0.2s;
        }

        .card:hover { transform: translateY(-5px); }

        .card h3 { 
            margin-top: 0; 
            display: flex; 
            align-items: center; 
            gap: 10px; 
            color: var(--dgo-purple);
        }

        .icon-box {
            width: 40px;
            height: 40px;
            background: var(--dgo-gradient);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
        }

        /* Financial Section */
        .section-title {
            font-size: 1.4rem;
            border-left: 5px solid var(--dgo-pink);
            padding-left: 15px;
            margin: 40px 0 20px 0;
            font-weight: 700;
        }

        .table-wrapper {
            background: #fff;
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid #e2e8f0;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th {
            background: #f1f5f9;
            padding: 18px;
            text-align: left;
            font-size: 0.85rem;
            color: var(--text-muted);
            text-transform: uppercase;
        }

        td { padding: 18px; border-bottom: 1px solid #f1f5f9; }

        .market-price { color: var(--text-muted); text-decoration: line-through; }
        .dgo-price { 
            color: var(--success); 
            font-weight: 700; 
            background: #ecfdf5; 
            padding: 5px 12px; 
            border-radius: 6px; 
        }

        .total-row {
            background: #0f172a;
            color: white;
            font-weight: 700;
            font-size: 1.1rem;
        }

        /* Media Buttons */
        .media-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
            margin-top: 20px;
        }

        .news-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            padding: 15px 10px;
            background: white;
            border: 1px solid #e2e8f0;
            border-radius: 10px;
            text-decoration: none;
            color: var(--text-main);
            font-weight: 600;
            font-size: 0.85rem;
            transition: all 0.3s ease;
        }

        .news-btn:hover {
            background: var(--dgo-gradient);
            color: white;
            border-color: transparent;
            box-shadow: 0 10px 20px rgba(217, 70, 239, 0.2);
        }

        /* Global Outreach Block */
        .global-outreach {
            background: var(--dgo-gradient);
            color: white;
            padding: 40px;
            border-radius: 16px;
            margin: 40px 0;
        }

        footer {
            text-align: center;
            padding: 40px;
            color: var(--text-muted);
            font-size: 0.9rem;
            border-top: 1px solid #f1f5f9;
        }

        @media (max-width: 768px) {
            .summary-grid, .media-grid { grid-template-columns: 1fr; }
            .branding-header { flex-direction: column; text-align: center; gap: 20px; }
        }
    </style>
</head>
<body>

<div class="report-container">
    <!-- Branding Header -->
    <div class="branding-header">
        <div class="logo-placeholder">
            <!-- REPLACE THIS LINK WITH YOUR REAL LOGO URL -->
            D GO
        </div>
        <div class="project-badge">Board Presentation 2026</div>
    </div>

    <div class="content">
        <div class="headline-section">
            <h1>Dimag Ghochne Manche</h1>
            <p>End-to-End Branding & Global Outreach Impact Report</p>
            <div style="margin-top: 10px; font-size: 0.9rem;">
                <strong>Lead:</strong> Aashish Lamichhane &nbsp; | &nbsp; 
                <strong>Partner:</strong> Ujwal Thapa Foundation
            </div>
        </div>

        <div class="summary-grid">
            <div class="card">
                <h3><div class="icon-box"><i class="fas fa-rocket"></i></div> Soft Launch</h3>
                <p>Strategically used the documentary premiere to introduce the <strong>new D Go logo and name</strong>, positioning the platform as a socially conscious leader in Nepal’s OTT ecosystem.</p>
            </div>
            <div class="card">
                <h3><div class="icon-box"><i class="fas fa-chart-pie"></i></div> Efficiency</h3>
                <p>Achieved massive visibility across <strong>16 top-tier media outlets</strong> with <strong>Zero Marketing Spend</strong>, saving significant capital while building high brand equity.</p>
            </div>
        </div>

        <div class="section-title">Strategic Branding Execution</div>
        <div class="summary-grid" style="grid-template-columns: repeat(3, 1fr);">
            <div class="card" style="text-align: center;">
                <i class="fas fa-paint-brush" style="font-size: 2rem; color: var(--dgo-purple); margin-bottom: 15px;"></i>
                <h4>Visual Identity</h4>
                <p style="font-size: 0.85rem; color: var(--text-muted);">New assets with BLQ team to reinforce branding.</p>
            </div>
            <div class="card" style="text-align: center;">
                <i class="fas fa-bullhorn" style="font-size: 2rem; color: var(--dgo-pink); margin-bottom: 15px;"></i>
                <h4>Organic Engagement</h4>
                <p style="font-size: 0.85rem; color: var(--text-muted);">5 targeted viral clips distributed globally.</p>
            </div>
            <div class="card" style="text-align: center;">
                <i class="fas fa-newspaper" style="font-size: 2rem; color: var(--dgo-red); margin-bottom: 15px;"></i>
                <h4>Editorial PR</h4>
                <p style="font-size: 0.85rem; color: var(--text-muted);">National news coverage via strategic press releases.</p>
            </div>
        </div>

        <div class="section-title">Financial Performance vs. Market Value</div>
        <div class="table-wrapper">
            <table>
                <thead>
                    <tr>
                        <th>Media Category</th>
                        <th>Coverage Summary</th>
                        <th>Market Rate (Est.)</th>
                        <th>D Go Actual Cost</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>Top-Tier Portals</strong></td>
                        <td>Setopati, Onlinekhabar, Nagarik News</td>
                        <td class="market-price">NPR 85,000</td>
                        <td><span class="dgo-price">NPR 0</span></td>
                    </tr>
                    <tr>
                        <td><strong>Social Authority</strong></td>
                        <td>Viral post on RONB</td>
                        <td class="market-price">NPR 65,000</td>
                        <td><span class="dgo-price">NPR 0</span></td>
                    </tr>
                    <tr>
                        <td><strong>Mainstream News</strong></td>
                        <td>5 Articles (Baahrakhari, Lokaantar, etc.)</td>
                        <td class="market-price">NPR 75,000</td>
                        <td><span class="dgo-price">NPR 0</span></td>
                    </tr>
                    <tr>
                        <td><strong>Tech & Business</strong></td>
                        <td>7 Features (Techpana, ICT Frame, etc.)</td>
                        <td class="market-price">NPR 55,000</td>
                        <td><span class="dgo-price">NPR 0</span></td>
                    </tr>
                    <tr>
                        <td><strong>Creative Assets</strong></td>
                        <td>5 BLQ Designed Social Media Clips</td>
                        <td class="market-price">NPR 20,000</td>
                        <td><span class="dgo-price">NPR 0</span></td>
                    </tr>
                    <tr class="total-row">
                        <td colspan="2" style="text-align: right; padding-right: 30px;">TOTAL EARNED MEDIA VALUE</td>
                        <td>NPR 3,00,000</td>
                        <td style="color: #4ade80;">NPR 0</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="global-outreach">
            <h3 style="margin-top: 0;"><i class="fas fa-globe-americas"></i> Global Diaspora Strategy</h3>
            <p>By leveraging 16 verified media links, we built massive credibility for the Nepali diaspora in the **USA, Australia, and Europe**. The narrative successfully combined the D Go platform's seamless UX with the impactful mission of the **Ujwal Thapa Foundation**, converting international viewers into long-term brand advocates.</p>
        </div>

        <div class="section-title">Verified Media Coverage (16 Links)</div>
        <div class="media-grid">
            <a href="https://setopati.com" target="_blank" class="news-btn">Setopati <i class="fas fa-external-link-alt"></i></a>
            <a href="https://onlinekhabar.com" target="_blank" class="news-btn">Onlinekhabar <i class="fas fa-external-link-alt"></i></a>
            <a href="#" target="_blank" class="news-btn">Online Pana <i class="fas fa-external-link-alt"></i></a>
            <a href="https://nepalkhabar.com" target="_blank" class="news-btn">Nepal Khabar <i class="fas fa-external-link-alt"></i></a>
            <a href="#" target="_blank" class="news-btn">Artapana <i class="fas fa-external-link-alt"></i></a>
            <a href="#" target="_blank" class="news-btn">Arthapath <i class="fas fa-external-link-alt"></i></a>
            <a href="#" target="_blank" class="news-btn">Artha Chautari <i class="fas fa-external-link-alt"></i></a>
            <a href="https://ictframe.com" target="_blank" class="news-btn">ICT Frame <i class="fas fa-external-link-alt"></i></a>
            <a href="https://baahrakhari.com" target="_blank" class="news-btn">Baahrakhari <i class="fas fa-external-link-alt"></i></a>
            <a href="#" target="_blank" class="news-btn">Breaknlinks <i class="fas fa-external-link-alt"></i></a>
            <a href="https://bizpati.com" target="_blank" class="news-btn">Bizpati <i class="fas fa-external-link-alt"></i></a>
            <a href="https://lokaantar.com" target="_blank" class="news-btn">Lokaantar <i class="fas fa-external-link-alt"></i></a>
            <a href="https://techpana.com" target="_blank" class="news-btn">Techpana <i class="fas fa-external-link-alt"></i></a>
            <a href="https://nagariknews.nagariknetwork.com" target="_blank" class="news-btn">Nagarik News <i class="fas fa-external-link-alt"></i></a>
            <a href="#" target="_blank" class="news-btn">RONB <i class="fab fa-facebook"></i></a>
            <a href="#" target="_blank" class="news-btn">Online Pana FB <i class="fab fa-facebook"></i></a>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 D Go Media Group. Confidential Performance Audit.</p>
    </footer>
</div>

</body>
</html># dimag
