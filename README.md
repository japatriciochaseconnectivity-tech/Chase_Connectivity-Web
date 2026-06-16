<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chase Connectivity | Enterprise Telecom & Carrier Operations</title>
    <style>
        /* Modern Reset & Corporate Color Palette based on image */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --navy-dark: #000c24;
            --blue-main: #002fbe;
            --gold-bright: #ffbd14;
            --gold-dark: #f0a500;
            --text-light: #ffffff;
            --text-dark: #000c24;
            --bg-light: #f8fafc;
        }

        body {
            color: var(--text-dark);
            background-color: var(--bg-light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation */
        header {
            background: rgba(0, 12, 36, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 2px solid var(--gold-bright);
        }

        .navbar {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        .logo-container img {
            height: 50px;
            object-fit: contain;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-light);
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--gold-bright);
        }

        /* Hero Section with Custom Wave Background Integration */
        .hero {
            position: relative;
            background: linear-gradient(180deg, var(--navy-dark) 0%, var(--blue-main) 70%);
            color: var(--text-light);
            padding: 180px 20px 180px;
            text-align: center;
            overflow: hidden;
        }

        .hero-waves {
            position: absolute;
            top: 20%;
            left: -10%;
            width: 120%;
            height: 60%;
            background-image: radial-gradient(rgba(255,255,255,0.15) 1px, transparent 0);
            background-size: 24px 24px;
            transform: skewY(-4deg);
            pointer-events: none;
        }

        .hero-content {
            max-width: 850px;
            margin: 0 auto;
            position: relative;
            z-index: 10;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 25px;
            line-height: 1.2;
            font-weight: 800;
        }

        .hero h1 span {
            color: var(--gold-bright);
            text-shadow: 0 2px 10px rgba(240, 165, 0, 0.3);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 40px;
            opacity: 0.9;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(135deg, var(--gold-bright) 0%, var(--gold-dark) 100%);
            color: var(--navy-dark);
            padding: 15px 35px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 700;
            box-shadow: 0 5px 15px rgba(255, 189, 20, 0.4);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 189, 20, 0.6);
        }

        /* The Gold/Yellow Wave Curve Transition from image */
        .wave-container {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            overflow: hidden;
            line-height: 0;
            transform: rotate(180deg);
        }

        .wave-container svg {
            position: relative;
            display: block;
            width: calc(140% + 1.3px);
            height: 110px;
        }

        .wave-container .shape-fill {
            fill: var(--gold-bright);
        }

        /* Services Section (Transitions from the Gold Wave) */
        .services {
            background: linear-gradient(180deg, var(--gold-bright) 0%, #fffde6 120px, #ffffff 100%);
            padding: 120px 20px 80px;
            position: relative;
        }

        .section-title {
            text-align: center;
            font-size: 2.8rem;
            margin-bottom: 20px;
            color: var(--navy-dark);
            font-weight: 700;
        }

        .section-subtitle {
            text-align: center;
            max-width: 600px;
            margin: 0 auto 60px;
            color: #55657e;
        }

        .services-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
        }

        .service-card {
            background: #ffffff;
            padding: 40px 35px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 12, 36, 0.05);
            border-bottom: 5px solid var(--blue-main);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 31, 190, 0.15);
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--blue-main);
        }

        /* Integrated Due Diligence Section */
        .sop-section {
            padding: 100px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .sop-container {
            background: #ffffff;
            border-radius: 16px;
            box-shadow: 0 15px 40px rgba(0, 12, 36, 0.08);
            border: 1px solid #e2e8f0;
            overflow: hidden;
        }

        .sop-header {
            background: var(--navy-dark);
            color: var(--text-light);
            padding: 25px 30px;
            border-bottom: 4px solid var(--gold-bright);
        }

        .sop-header h2 {
            font-size: 1.8rem;
            letter-spacing: 0.5px;
        }

        .sop-header p {
            color: var(--gold-bright);
            font-size: 0.9rem;
            font-weight: bold;
            margin-top: 5px;
        }

        .sop-row {
            display: grid;
            grid-template-columns: 280px 1fr;
            border-bottom: 1px solid #e2e8f0;
            transition: background 0.2s ease;
        }

        .sop-row:last-child {
            border-bottom: none;
        }

        .sop-row:hover {
            background: #f8fafc;
        }

        .sop-label {
            background: rgba(0, 47, 190, 0.02);
            padding: 30px;
            font-weight: 700;
            color: var(--blue-main);
            border-right: 1px solid #e2e8f0;
            display: flex;
            align-items: center;
        }

        .sop-content {
            padding: 30px;
        }

        .sop-content ul {
            list-style: none;
        }

        .sop-content li {
            position: relative;
            padding-left: 25px;
            margin-bottom: 12px;
            color: #334155;
        }

        .sop-content li::before {
            content: "✓";
            position: absolute;
            left: 0;
            top: 0;
            color: var(--gold-dark);
            font-weight: bold;
        }

        .sop-content .highlight-time {
            display: inline-block;
            background: #fef3c7;
            color: #92400e;
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 0.85rem;
            font-weight: 600;
        }

        /* Infrastructure Panel */
        .infrastructure {
            background: var(--navy-dark);
            color: var(--text-light);
            padding: 100px 20px;
            position: relative;
        }

        .infra-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 60px;
        }

        .infra-text {
            flex: 1;
            min-width: 300px;
        }

        .infra-text h2 {
            font-size: 2.5rem;
            margin-bottom: 25px;
            color: var(--gold-bright);
        }

        .infra-stats {
            flex: 1;
            min-width: 300px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
        }

        .stat-box {
            background: rgba(255, 255, 255, 0.05);
            padding: 35px;
            border-radius: 12px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .stat-box h4 {
            font-size: 3rem;
            color: var(--gold-bright);
            margin-bottom: 10px;
        }

        /* Contact Section */
        .contact {
            padding: 100px 20px;
            max-width: 650px;
            margin: 0 auto;
            text-align: center;
        }

        .contact form {
            margin-top: 40px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .contact input, .contact textarea {
            padding: 18px;
            border: 2px solid #e2e8f0;
            border-radius: 8px;
            font-size: 1rem;
            outline: none;
            transition: border-color 0.3s ease;
            width: 100%;
        }

        .contact input:focus, .contact textarea:focus {
            border-color: var(--blue-main);
        }

        /* Footer */
        footer {
            background: #000614;
            color: rgba(255, 255, 255, 0.6);
            padding: 40px 20px;
            text-align: center;
            font-size: 0.95rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero h1 { font-size: 2.4rem; }
            .sop-row { grid-template-columns: 1fr; }
            .sop-label { border-right: none; border-bottom: 1px solid #e2e8f0; padding: 15px 30px; }
            .infra-stats { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <!-- Header / Navigation -->
    <header>
        <div class="navbar">
            <div class="logo-container">
                <img src="https://lh3.googleusercontent.com/d/1C8iXPdVlY9IJhqnUV4D-hUWU_UEj4gSL" alt="Chase Connectivity Logo" onerror="this.onerror=null; this.src='https://via.placeholder.com/220x50/000c24/ffffff?text=Chase+Connectivity';">
            </div>
            <ul class="nav-links">
                <li><a href="#services">Services</a></li>
                <li><a href="#due-diligence">Carrier Dashboard</a></li>
                <li><a href="#infrastructure">Infrastructure</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-waves"></div>
        <div class="hero-content">
            <h1>High-Speed Infrastructure <span>Engineered for Reliability</span></h1>
            <p>Providing robust point-to-point connections, premium dark fiber deployment, and carrier-grade IP Transit tailored for modern enterprises.</p>
            <a href="#due-diligence" class="btn">View Operations Manual</a>
        </div>

        <div class="wave-container">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M985.66,92.83C906.67,72,823.78,31,743.84,14.19c-82.26-17.34-168.06-16.33-250.45.39-57.84,11.73-114,31.07-172,41.86A600.21,600.21,0,0,1,0,27.35V120H1200V95.8C1132.19,118.92,1055.71,111.31,985.66,92.83Z" class="shape-fill"></path>
            </svg>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <h2 class="section-title">Our Enterprise Solutions</h2>
        <p class="section-subtitle">Delivering high-capacity telecommunications solutions across strategic regional and core Metro Manila hubs.</p>
        <div class="services-grid">
            <div class="service-card">
                <h3>Fiber Optic Deployment</h3>
                <p>End-to-end civil works, customized municipal path clearing, and precise multi-core optical fiber layouts designed for future expansions.</p>
            </div>
            <div class="service-card">
                <h3>High-Capacity Backhaul</h3>
                <p>Dedicated high-speed loop systems and point-to-point transport networks that link major regional hubs safely with minimal hops.</p>
            </div>
            <div class="service-card">
                <h3>Resilient Peering & IP</h3>
                <p>Strategic BGP route handling and multi-homed upstream paths ensuring that service disruptions are prevented automatically.</p>
            </div>
        </div>
    </section>

    <!-- Interactive Due Diligence Section -->
    <section id="due-diligence" class="sop-section">
        <h2 class="section-title" style="margin-bottom: 10px;">Carrier Operations Protocol</h2>
        <p class="section-subtitle" style="margin-bottom: 40px;">Standard operating procedures enforced by Chase Connectivity to guarantee quality delivery.</p>
        
        <div class="sop-container">
            <div class="sop-header">
                <h2>CARRIER TEAM: DUE DILIGENCE</h2>
                <p>INTERNAL DISPATCH & COMPLIANCE FRAMEWORK</p>
            </div>

            <div class="sop-row">
                <div class="sop-label">Feasibility</div>
                <div class="sop-content">
                    <ul>
                        <li><strong>Data Verification:</strong> Always double check details. Ensure account name, BW requirements & service, complete address, and coordinates are complete.</li>
                        <li><strong>Circuit Matching:</strong> For DLL accounts, double check Site A and Site B. For IX accounts, verify the Rack ID and transport requirements.</li>
                        <li><strong>Group Dispatch:</strong> Submit requirements to the preferred telco. Right after submission, notify the account manager in the group chat immediately.</li>
                        <li><strong>Escalation Window:</strong> Timeline for checking is <span class="highlight-time">7 working days</span>. Send a strict follow-up to the AM on day 5.</li>
                        <li><strong>Post-Approval:</strong> Once verified feasible, inform the assigned sales team to draft contracts and initiate the implementation stage. Check the shared matrix regularly for live updates.</li>
                    </ul>
                </div>
            </div>

            <div class="sop-row">
                <div class="sop-label">Pricing Approval</div>
                <div class="sop-content">
                    <ul>
                        <li><strong>Authorization:</strong> Rate requests are strictly subject to the verified approval of the Carrier Head.</li>
                        <li><strong>Turnaround Target:</strong> Maximum waiting time for rate validation is within <span class="highlight-time">2 days</span> (Fastest resolutions processed same-day).</li>
                        <li><strong>Provider Dependency:</strong> Final wholesale costing directly depends on the chosen backhaul/service provider parameters.</li>
                    </ul>
                </div>
            </div>

            <div class="sop-row">
                <div class="sop-label">Job Order (JO)</div>
                <div class="sop-content">
                    <ul>
                        <li><strong>Execution Trigger:</strong> Carrier Head will initiate the JO request to the preferred telco only when a signed proposal from the end client is securely on hand.</li>
                        <li><strong>Document Requirement:</strong> A signed quote from the preferred telco is strictly required from the AM to process the transaction.</li>
                        <li><strong>Turnaround Window:</strong> Maximum waiting window is <span class="highlight-time">7 days</span>, minimum processing is <span class="highlight-time">3 days</span>.</li>
                    </ul>
                </div>
            </div>

            <div class="sop-row">
                <div class="sop-label">Implementation</div>
                <div class="sop-content">
                    <ul>
                        <li><strong>Critical Phase:</strong> Attention to detail and transparent deployment timelines must be aligned directly with the AM beforehand. Constant back-to-back updates are required.</li>
                        <li><strong>Dual-Ended Coordination:</strong> Active loop synchronization from the assigned PM to the POC or the end client. Ensure clear coordination across both sites.</li>
                        <li><strong>Site Survey:</strong> Secure the end client POC contact information, map out their preferred schedule for field surveys, and route immediately back to the PM.</li>
                        <li><strong>Activation Protocol:</strong> Maintain open channels up to activation day. Activations are strictly handled by the assigned Field Engineer (FE) of the telco.</li>
                        <li><strong>Verification Handover:</strong> Secure official speedtest results confirming subscribed capacity is reached. A signed <strong>Service Acceptance Form</strong> must be archived upon activation.</li>
                        <li><strong>SLA Trial:</strong> A <span class="highlight-time">7-day testing window</span> is granted to the end client to monitor circuit stability. Billing automatically commences on Day 8.</li>
                    </ul>
                </div>
            </div>

            <div class="sop-row">
                <div class="sop-label">Technical Reporting</div>
                <div class="sop-content">
                    <ul>
                        <li><strong>Triage Responsiveness:</strong> Technical concerns given by the end client must be acknowledged as soon as possible. Maintain high attentiveness to all Viber operational groups for real-time ticket alerts.</li>
                        <li><strong>Categorization:</strong> Instantly diagnose the link state: Is it a complete down circuit or an intermittent jitter/packet loss incident?</li>
                        <li><strong>Communication Rule:</strong> Never leave active threads hanging without replies. Provide clear status metrics such as <em>"For a while"</em> or <em>"Currently checking"</em> to state commitment.</li>
                    </ul>
                </div>
            </div>

            <div class="sop-row">
                <div class="sop-label">Data Processing</div>
                <div class="sop-content">
                    <ul>
                        <li><strong>Accuracy Mandate:</strong> Double-check every data parameter before relaying it outward to the client. Always confirm and ask internally if you are unsure of any technical metric.</li>
                    </ul>
                </div>
            </div>

        </div>
    </section>

    <!-- Infrastructure Panel -->
    <section id="infrastructure" class="infrastructure">
        <div class="infra-container">
            <div class="infra-text">
                <h2>Built For Uninterrupted Performance</h2>
                <p>From underground path deployments to highly dense technical nodes, Chase Connectivity delivers state-of-the-art telecommunication pathways optimized for uptime across critical business hubs.</p>
            </div>
            <div class="infra-stats">
                <div class="stat-box">
                    <h4>99.99%</h4>
                    <p>SLA Guarded Uptime</p>
                </div>
                <div class="stat-box">
                    <h4>&lt; 5ms</h4>
                    <p>Core Node Latency</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Form Section pointing to Formspree -->
    <section id="contact" class="contact">
        <h2>Initiate Site Feasibility Check</h2>
        <p>Send over your geographical targets or bandwidth requisites, and our technical field crew will get back to you promptly.</p>
        
        <!-- Pinalitan ang action para dumeretso sa Formspree setup para sa iyong email -->
        <form action="https://formspree.io/f/xoqorjle" method="POST">
            <input type="text" name="Company Name" placeholder="Corporate / Business Name" required>
            <!-- May 'replyto' attribute para kapag sinagot mo ang email, dederetso sa nag-submit -->
            <input type="email" name="_replyto" placeholder="Corporate Email Address" required>
            <input type="text" name="Site Target" placeholder="Target Site Area (Coordinates or City)" required>
            <textarea name="Project Requirements" rows="5" placeholder="Tell us about your infrastructure load demands..." required></textarea>
            
            <!-- Custom routing settings para sa malinis na interface -->
            <input type="hidden" name="_subject" value="New Chase Connectivity Technical Inquiry Found!">
            
            <button type="submit" class="btn" style="border:none; cursor:pointer; width: 100%;">Submit Technical Inquiry</button>
        </form>
    </section>

    <!-- Footer Area -->
    <footer>
        <p>© 2026 Chase Connectivity. Secure, Scalable, Seamless Infrastructure Solutions.</p>
    </footer>

</body>
</html>
