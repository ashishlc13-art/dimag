<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DGO | DGM Impact Report</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    
    <style>
        :root {
            /* DGO Logo Palette */
            --dgo-purple: #8b5cf6;
            --dgo-pink: #d946ef;
            --dgo-red: #f43f5e;
            --dgo-gradient: linear-gradient(135deg, #8b5cf6 0%, #d946ef 50%, #f43f5e 100%);
            
            --bg-base: #f8fafc;
            --text-heading: #0f172a;
            --text-body: #475569;
            --white: #ffffff;
            --success: #10b981;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg-base);
            color: var(--text-body);
            margin: 0;
            padding: 40px 20px;
            line-height: 1.6;
        }

        .main-container {
            max-width: 1100px;
            margin: 0 auto;
            background: var(--white);
            border-radius: 30px;
            box-shadow: 0 25px 80px rgba(0,0,0,0.06);
            overflow: hidden;
            border: 1px solid #e2e8f0;
        }

        /* Executive Header */
        header {
            padding: 50px;
            background: linear-gradient(to right, #ffffff, #f1f5f9);
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #e2e8f0;
        }

        .logo-area {
            font-size: 3rem;
            font-weight: 800;
            letter-spacing: -3px;
            display: flex;
            gap: 2px;
        }
        .logo-d { color: var(--dgo-purple); }
        .logo-g { color: var(--dgo-pink); }
        .logo-o { color: var(--dgo-red); }

        .meta-area { text-align: right; }
        .meta-area h1 { 
            margin: 0; 
            font-size: 1.6rem; 
            font-weight: 800; 
            color: var(--text-heading);
            letter-spacing: 1px;
        }
        .meta-area p { margin: 5px 0 0; font-weight: 600; color: var(--dgo-pink); text-transform: uppercase; font-size: 0.8rem; }

        /* Content Sections */
        .content { padding: 50px; }

        .grid-summary {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
            margin-bottom: 50px;
        }

        .card {
            padding: 35px;
            border-radius: 24px;
            background: #fff;
            border: 1px solid #f1f5f9;
            box-shadow: 0 10px 30px rgba(0,0,0,0.02);
            position: relative;
        }
        .card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 6px; height: 100%;
            background: var(--dgo-gradient);
            border-radius: 24px 0 0 24px;
        }

        .card h3 { margin-top: 0; color: var(--text-heading); font-size: 1.25rem; }
        .card p { font-size: 0.95rem; color: var(--text-body); }

        /* Financial Table */
        .table-section { margin-bottom: 60px; }
        .section-title {
            font-size: 1.1rem;
            font-weight: 800;
            color: var(--text-heading);
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .section-title::after { content: ''; flex-grow: 1; height: 1px; background: #e2e8f0; }

        .table-container {
            border-radius: 20px;
            border: 1px solid #e2e8f0;
            overflow: hidden;
        }

        table { width: 100%; border-collapse: collapse; background: #fff; }
        th { background: #f8fafc; padding: 20px; text-align: left; font-size: 0.7rem; text-transform: uppercase; color: var(--text-heading); border-bottom: 1px solid #e2e8f0; }
        td { padding: 20px; border-bottom: 1px solid #f1f5f9; font-size: 0.95rem; }

        .market-val { color: #94a3b8; text-decoration: line-through; }
        .actual-val { 
            color: var(--success); 
            font-weight: 800; 
            background: #f0fdf4; 
            padding: 6px 15px; 
            border-radius: 8px;
            display: inline-block;
        }

        .total-banner {
            background: var(--text-heading);
            color: white;
            padding: 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* Media Link Buttons */
        .media-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
        }

        .btn-link {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 18px 10px;
            background: white;
            border: 1px solid #e2e8f0;
            border-radius: 14px;
            text-decoration: none;
            color: var(--text-heading);
            font-weight: 700;
            font-size: 0.8rem;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .btn-link:hover {
            border-color: var(--dgo-pink);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(217, 70, 239, 0.1);
            color: var(--dgo-purple);
        }

        .featured-ronb {
            background: #fffbeb;
            border: 2px solid #f59e0b;
        }

        /* Global Outreach Section */
        .impact-footer {
            margin-top: 60px;
            background: var(--dgo-gradient);
            padding: 45px;
            border-radius: 24px;
            color: white;
        }

        footer {
            padding: 40px;
            text-align: center;
            font-size: 0.8rem;
            color: #94a3b8;
            font-weight: 600;
        }

        @media (max-width: 900px) {
            .grid-summary, .media-grid { grid-template-columns: 1fr; }
            header { flex-direction: column; text-align: center; gap: 20px; }
            .meta-area { text-align: center; }
        }
    </style>
</head>
<body>

<div class="main-container">
    <!-- Header Area -->
    <header>
        <div class="logo-area">
            <span class="logo-d">D</span><span class="logo-g">G</span><span class="logo-o">O</span>
        </div>
        <div class="meta-area">
            <h1>DGM OUTREACH REPORT</h1>
            <p>Partners: DGO x Ujwal Thapa Foundation</p>
        </div>
    </header>

    <div class="content">
        <!-- Summary Section -->
        <div class="grid-summary">
            <div class="card">
                <h3>Executive Branding</h3>
                <p>The DGM premiere served as the official <strong>Soft Launch for DGO</strong>. By aligning with a social cause, we secured a high-authority brand position in the Nepali OTT market from Day 1.</p>
            </div>
            <div class="card">
                <h3>Capital Efficiency</h3>
                <p>Generated nationwide organic reach across 16 major platforms with <strong>Zero Marketing Cash Outflow</strong>. We preserved company liquidity while maximizing earned media value.</p>
            </div>
        </div>

        <!-- Financial Performance Table -->
        <div class="table-section">
            <div class="section-title">Value Audit & Efficiency</div>
            <div class="table-container">
                <table>
                    <thead>
                        <tr>
                            <th>Category</th>
                            <th>Platform Coverage</th>
                            <th>Market Value (Est.)</th>
                            <th>DGO Actual Cost</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Top-Tier Portals</strong></td>
                            <td>Setopati, Onlinekhabar, Nagarik News</td>
                            <td><span class="market-val">NPR 85,000</span></td>
                            <td><span class="actual-val">NPR 0</span></td>
                        </tr>
                        <tr>
                            <td><strong>Social Authority</strong></td>
                            <td>Routine of Nepal Banda (Viral Feature)</td>
                            <td><span class="market-val">NPR 65,000</span></td>
                            <td><span class="actual-val">NPR 0</span></td>
                        </tr>
                        <tr>
                            <td><strong>Mainstream News</strong></td>
                            <td>5 National Portals (Lokaantar, Baahrakhari, etc.)</td>
                            <td><span class="market-val">NPR 75,000</span></td>
                            <td><span class="actual-val">NPR 0</span></td>
                        </tr>
                        <tr>
                            <td><strong>Tech & Business</strong></td>
                            <td>7 Specialized Outlets (Techpana, Bizpati, etc.)</td>
                            <td><span class="market-val">NPR 55,000</span></td>
                            <td><span class="actual-val">NPR 0</span></td>
                        </tr>
                        <tr>
                            <td><strong>Visual Assets</strong></td>
                            <td>5 High-Quality BLQ Brand Clips</td>
                            <td><span class="market-val">NPR 20,000</span></td>
                            <td><span class="actual-val">NPR 0</span></td>
                        </tr>
                    </tbody>
                </table>
                <div class="total-banner">
                    <span style="font-weight: 400; opacity: 0.8; font-size: 0.8rem; text-transform: uppercase; letter-spacing: 2px;">Total Earned Media Value</span>
                    <span style="font-size: 1.6rem; font-weight: 800;">NPR 3,00,000 &nbsp;→&nbsp; <span style="color: var(--success);">NPR 0</span></span>
                </div>
            </div>
        </div>

        <!-- Media Matrix -->
        <div class="section-header">
            <div class="section-title">Media Outreach Appendix</div>
        </div>
        
        <div class="media-grid">
            <!-- Specific Viral Link Provided -->
            <a href="https://www.facebook.com/share/p/14WohGinWvC/?mibextid=wwXIfr" target="_blank" class="btn-link featured-ronb">
                <i class="fab fa-facebook" style="color: #1877F2;"></i> RONB (Viral)
            </a>
            
            <a href="https://setopati.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> Setopati</a>
            <a href="https://onlinekhabar.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> Onlinekhabar</a>
            <a href="https://nepalkhabar.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> Nepal Khabar</a>
            <a href="https://baahrakhari.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> Baahrakhari</a>
            <a href="https://techpana.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> Techpana</a>
            <a href="https://lokaantar.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> Lokaantar</a>
            <a href="https://nagariknews.nagariknetwork.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> Nagarik News</a>
            <a href="https://ictframe.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> ICT Frame</a>
            <a href="https://bizpati.com" target="_blank" class="btn-link"><i class="fas fa-external-link-alt"></i> Bizpati</a>
            <a href="#" target="_blank" class="btn-link">Online Pana</a>
            <a href="#" target="_blank" class="btn-link">Artapana</a>
            <a href="#" target="_blank" class="btn-link">Arthapath</a>
            <a href="#" target="_blank" class="btn-link">Artha Chautari</a>
            <a href="#" target="_blank" class="btn-link">Breaknlinks</a>
            <a href="#" target="_blank" class="btn-link">Online Pana FB</a>
        </div>

        <!-- Strategy Footer -->
        <div class="impact-footer">
            <h3 style="margin-top:0;"><i class="fas fa-globe-americas"></i> Global Outreach Strategy</h3>
            <p style="margin:0; opacity:0.95; font-weight: 500;">
                By utilizing the credibility of 16 verified media links, we positioned **DGM** as a must-watch documentary for the Nepali diaspora in the USA, Australia, and Europe. This strategy successfully leveraged the **DGO** platform’s global scalability and ensured that international viewership directly translated into support for the **Ujwal Thapa Foundation**.
            </p>
        </div>
    </div>

    <footer>
        CONFIDENTIAL BOARD REPORT | DGO MEDIA GROUP | APRIL 2026
    </footer>
</div>

</body>
</html>
