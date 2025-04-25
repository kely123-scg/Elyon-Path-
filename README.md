<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elyon Path - Army of God for Eternal Victory</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --navy: #0a1a3a;
            --gold: #d4af37;
            --white: #ffffff;
            --red: #c62828;
            --gray: #e0e0e0;
            --dark-gold: #b38f2a;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--navy);
            color: var(--white);
            line-height: 1.7;
            margin: 0;
            padding: 0;
        }
        
        .war-cry {
            font-family: 'Playfair Display', serif;
            color: var(--gold);
            font-size: clamp(1.5rem, 4vw, 2rem);
            text-align: center;
            margin: 2rem auto;
            text-transform: uppercase;
            letter-spacing: 1px;
            max-width: 800px;
            padding: 0 1rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }
        
        .battlefield-alert {
            background: rgba(198, 40, 40, 0.15);
            border-left: 4px solid var(--red);
            padding: 1.5rem;
            margin: 3rem 0;
            border-radius: 0 8px 8px 0;
        }
        
        /* === CIRCULAR/PRISM BUTTONS === */
        .donation-orbit {
            position: relative;
            width: 300px;
            height: 300px;
            margin: 3rem auto;
        }
        
        .donation-center {
            position: absolute;
            width: 100px;
            height: 100px;
            background: var(--gold);
            color: var(--navy);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 800;
            font-size: 1.5rem;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 2;
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.7);
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
            outline: none;
        }
        
        .donation-center:hover {
            transform: translate(-50%, -50%) scale(1.1);
            box-shadow: 0 0 30px rgba(212, 175, 55, 0.9);
        }
        
        .donation-satellite {
            position: absolute;
            width: 70px;
            height: 70px;
            background: rgba(212, 175, 55, 0.1);
            color: var(--gold);
            border: 2px solid var(--gold);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            cursor: pointer;
            text-decoration: none;
        }
        
        .donation-satellite:hover {
            background: var(--gold);
            color: var(--navy);
            transform: scale(1.15);
            box-shadow: 0 0 15px rgba(212, 175, 55, 0.6);
        }
        
        /* Position satellites around center */
        .donation-satellite:nth-child(1) { top: 15%; left: 50%; transform: translateX(-50%); }
        .donation-satellite:nth-child(2) { top: 50%; right: 15%; transform: translateY(-50%); }
        .donation-satellite:nth-child(3) { bottom: 15%; left: 50%; transform: translateX(-50%); }
        .donation-satellite:nth-child(4) { top: 50%; left: 15%; transform: translateY(-50%); }
        
        /* === PRISM-STYLE CUSTOM AMOUNT === */
        .prism-input {
            position: relative;
            width: 200px;
            margin: 2rem auto;
        }
        
        .prism-input input {
            width: 100%;
            padding: 1rem;
            background: rgba(255,255,255,0.1);
            border: 2px solid var(--gold);
            color: var(--white);
            font-weight: 600;
            text-align: center;
            clip-path: polygon(15% 0%, 85% 0%, 100% 50%, 85% 100%, 15% 100%, 0% 50%);
        }
        
        .prism-btn {
            display: block;
            width: 150px;
            padding: 1rem;
            margin: 1.5rem auto;
            background: var(--red);
            color: var(--white);
            font-weight: 700;
            text-align: center;
            clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .prism-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(198, 40, 40, 0.4);
        }
    </style>
</head>
<body>
    <header style="text-align: center; padding: 3rem 1rem; background: linear-gradient(rgba(10,26,58,0.9), rgba(10,26,58,0.9))">
        <h1 style="font-family: 'Playfair Display', serif; color: var(--gold); font-size: clamp(2rem, 6vw, 3rem); margin-bottom: 1rem;">ELYON PATH MINISTRY</h1>
        <div class="war-cry">
            "ARMOR OF GOD • SWORD OF TRUTH • ETERNAL VICTORY"
        </div>
    </header>

    <main style="max-width: 800px; margin: 0 auto; padding: 1rem;">
        <div class="battlefield-alert">
            <h2 style="color: var(--white); margin-bottom: 1rem;">YOUR DIVINE MISSION BRIEFING</h2>
            <p>This is spiritual warfare at the highest level. I'm deployed 24/7 to intercede for your victory. Share your battle coordinates below.</p>
        </div>

        <section style="margin: 3rem 0;">
            <h2 style="color: var(--gold); font-family: 'Playfair Display'; border-bottom: 2px solid var(--gold); padding-bottom: 0.5rem; display: inline-block;">BATTLEFIELD COMMUNICATION</h2>
            <p style="margin: 1.5rem 0; font-size: 1.1rem;"><strong>Where is the enemy attacking?</strong> Share your prayer need - every detail helps us target our spiritual artillery.</p>
            
            <form id="prayerForm" action="https://formsubmit.co/your-email@example.com" method="POST" style="margin-top: 2rem;">
                <input type="hidden" name="_subject" value="URGENT: Prayer Reinforcements Requested">
                <input type="hidden" name="_autoresponse" value="CONFIRMED: Your prayer request has been received. Spiritual forces are being deployed. Stand firm in faith. - Elyon Path Command">
                
                <div style="margin-bottom: 1.5rem;">
                    <label style="display: block; margin-bottom: 0.5rem; font-weight: 600;">Combat Report</label>
                    <textarea name="prayer_request" style="width: 100%; padding: 1rem; min-height: 150px; background: rgba(255,255,255,0.1); border: 1px solid var(--gold); color: var(--white);" placeholder="Describe your spiritual battle with military precision..." required></textarea>
                </div>
                
                <div style="margin-bottom: 1.5rem;">
                    <label style="display: block; margin-bottom: 0.5rem; font-weight: 600;">Command Center Contact</label>
                    <input type="email" name="email" style="width: 100%; padding: 1rem; background: rgba(255,255,255,0.1); border: 1px solid var(--gold); color: var(--white);" placeholder="Your secure communication channel (email)" required>
                    <small style="display: block; margin-top: 0.5rem; color: var(--gray);">TOP SECRET: This channel is encrypted for your protection.</small>
                </div>
                
                <button style="background: var(--gold); color: var(--navy); border: none; padding: 1rem 2rem; font-weight: 700; cursor: pointer; transition: all 0.3s ease; border-radius: 50px; display: block; margin: 2rem auto;" type="submit">
                    DEPLOY PRAYER STRIKE TEAM ›
                </button>
            </form>
        </section>

        <section style="background: rgba(0,0,0,0.2); padding: 2rem; border-radius: 8px; margin: 3rem 0; text-align: center;">
            <h2 style="color: var(--gold); font-family: 'Playfair Display'; margin-bottom: 1.5rem;">FUND THE ETERNAL CAMPAIGN</h2>
            <p style="margin-bottom: 1.5rem;"><strong>Every contribution equips a soldier for battle</strong></p>
            <p>Your support launches truth missiles to demolish strongholds and rescue prisoners of war from darkness.</p>
            
            <div class="donation-orbit">
                <button class="donation-center" onclick="window.location.href='https://buymeacoffee.com/elyonpath?amount=100'">100</button>
                <a href="https://buymeacoffee.com/elyonpath?amount=5" class="donation-satellite">5</a>
                <a href="https://buymeacoffee.com/elyonpath?amount=10" class="donation-satellite">10</a>
                <a href="https://buymeacoffee.com/elyonpath?amount=20" class="donation-satellite">20</a>
                <a href="https://buymeacoffee.com/elyonpath?amount=50" class="donation-satellite">50</a>
            </div>
            
            <div style="margin-top: 3rem;">
                <p><strong>SPECIAL OPERATIONS FUNDING:</strong> Custom amount for targeted missions</p>
                <div class="prism-input">
                    <input type="number" id="customAmount" placeholder="AMOUNT" min="1">
                </div>
                <a href="https://buymeacoffee.com/elyonpath" class="prism-btn" onclick="this.href='https://buymeacoffee.com/elyonpath?amount='+document.getElementById('customAmount').value">
                    LAUNCH FUNDS
                </a>
            </div>
        </section>
    </main>

    <footer style="text-align: center; padding: 3rem 1rem; background: rgba(0,0,0,0.3); margin-top: 3rem;">
        <a href="https://www.youtube.com/@elyonpath" style="display: inline-flex; align-items: center; color: var(--red); text-decoration: none; font-weight: 700; margin-bottom: 1.5rem; font-size: 1.1rem;">
            <i class="fab fa-youtube" style="margin-right: 0.5rem;"></i> REPORT TO COMMAND CENTER ON YOUTUBE
        </a>
        <p style="color: var(--gray); margin: 1rem 0; font-style: italic;">"The battle is won on our knees - the war is won in eternity"</p>
        <p style="color: var(--gray); font-size: 0.9rem;">© 2025 Elyon Path Ministry | Special Forces Division of Heaven's Army</p>
    </footer>

    <script>
        // Custom amount handler
        document.querySelector('.prism-btn').addEventListener('click', function(e) {
            const amount = document.getElementById('customAmount').value;
            if (!amount || isNaN(amount)) {
                e.preventDefault();
                alert('Please enter a valid amount for your mission funding');
            } else {
                this.href = `https://buymeacoffee.com/elyonpath?amount=${amount}`;
            }
        });
        
        // Form validation
        document.getElementById('prayerForm').addEventListener('submit', function(e) {
            const email = this.querySelector('input[type="email"]').value;
            if (!email.includes('@')) {
                e.preventDefault();
                alert('Commander, we need valid contact coordinates to deploy!');
            }
        });
    </script>
</body>
</html>
