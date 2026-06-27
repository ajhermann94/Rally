<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RALLY: Motivation Alarm</title>
    <style>
        /* --- CORE THEME & LAYOUT --- */
        :root {
            --bg-black: #080808;
            --text-white: #eeeeee;
            --crimson: #a81c1c; /* A deep, aggressive crimson */
            --crimson-hover: #e02424; /* A brighter red for feedback */
            --font-heavy: 'Inter', sans-serif; /* Placeholder: Use a bold, modern sans-serif */
        }

        body {
            margin: 0;
            padding: 0;
            background-color: var(--bg-black);
            color: var(--text-white);
            font-family: var(--font-heavy);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            text-rendering: optimizeLegibility;
        }

        /* --- BACKGROUND (THE CLOCK) --- */
        body::before {
            content: '';
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(135deg, rgba(8, 8, 8, 0.95) 0%, rgba(168, 28, 28, 0.25) 100%),
                        url('data:image/svg+xml,%3Csvg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" opacity="0.03"%3E%3Ccircle cx="50" cy="50" r="48" stroke="white" stroke-width="2" fill="none"/%3E%3Cpath d="M50 10 V50 L75 75" stroke="white" stroke-width="3"/%3E%3C/svg%3E'); /* Subtle alarm clock vector pattern */
            background-size: cover;
            filter: grayscale(100%) contrast(150%); /* High contrast, aggressive texture */
            z-index: -1;
        }

        /* --- THE LOGO/HERO SECTION --- */
        .rally-wrapper {
            text-align: center;
            max-width: 900px;
            width: 100%;
            padding: 40px;
        }

        .rally-header {
            font-size: 72px; /* massive header */
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: -2px;
            margin-bottom: 10px;
            background: linear-gradient(180deg, #fff 40%, #888);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 2px 2px 0px rgba(168, 28, 28, 0.5); /* Crimson shadow offset */
        }

        .rally-tagline {
            font-size: 24px;
            font-weight: 300;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: #ccc;
            margin-bottom: 60px;
            border-bottom: 1px solid var(--crimson);
            padding-bottom: 20px;
            display: inline-block;
        }

        /* --- GOGGINS/JOCKO INSPIRATION CALLOUT --- */
        .rally-callout {
            font-size: 18px;
            font-weight: 600;
            text-transform: uppercase;
            color: #eee;
            margin-bottom: 40px;
            padding: 15px;
            border-left: 5px solid var(--crimson);
            background: rgba(168, 28, 28, 0.1);
            display: inline-block;
        }

        /* --- DOCUMENTATION LINKS --- */
        .doc-container {
            margin-top: 50px;
        }

        .doc-list {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .doc-link {
            display: block;
            text-decoration: none;
            color: var(--bg-black);
            background-color: var(--text-white);
            font-size: 16px;
            font-weight: 800;
            text-transform: uppercase;
            padding: 15px 40px;
            border: 2px solid var(--text-white);
            transition: all 0.2s ease-in-out;
            cursor: pointer;
        }

        /* The hard-flip crimson interaction */
        .doc-link:hover {
            color: var(--text-white);
            background-color: var(--crimson);
            border-color: var(--crimson);
            transform: translateY(-3px); /* subtle aggressive lift */
            box-shadow: 0 10px 20px rgba(168, 28, 28, 0.3);
        }

        .doc-link:active {
            transform: translateY(-1px);
        }

    </style>
</head>
<body>

    <div class="rally-wrapper">
        <header>
            <h1 class="rally-header">Rally</h1>
            <p class="rally-tagline">Motivation Alarm</p>
        </header>

        <section>
            <p class="rally-callout">"Get After It." &nbsp; | &nbsp; "They Don't Know You."</p>
            <p>Wake up. No slow sunrise. No building soundtrack. <span style="color: var(--crimson); font-weight: bold;">HARD LOCK IN.</span></p>
        </section>

        <!-- Your Documentation and Support links (referencing image_62e343.png) -->
        <nav class="doc-container">
            <ul class="doc-list">
                <li><a href="docs/privacy.md" class="doc-link">Privacy Policy</a></li>
                <li><a href="docs/terms.md" class="doc-link">Terms of Use</a></li>
                <li><a href="docs/support.md" class="doc-link">Support &amp; Contact</a></li>
            </ul>
        </nav>
    </div>

</body>
</html>
