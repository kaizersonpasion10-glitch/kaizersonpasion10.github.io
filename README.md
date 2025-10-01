<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>E-commerce Flowchart Website</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            background: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 900px;
            margin: 30px auto;
            background: #fff;
            border-radius: 12px;
            box-shadow: 0 4px 16px rgba(0,0,0,0.08);
            padding: 30px;
        }
        h1 {
            text-align: center;
            color: #1565c0;
        }
        .flowchart {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 18px;
            margin-top: 30px;
        }
        .step {
            padding: 12px 28px;
            border-radius: 8px;
            font-size: 1.07em;
            min-width: 180px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(21,101,192,0.07);
            position: relative;
            background: #a5d6a7;
            color: #222;
            font-weight: 500;
        }
        .decision {
            background: #4fc3f7;
            color: #222;
            border-radius: 12px;
            min-width: 220px;
            font-style: italic;
        }
        .start, .end {
            background: #e57373;
            color: white;
            border-radius: 999px;
            font-weight: bold;
            min-width: 120px;
        }
        .arrow {
            width: 0; height: 0;
            border-left: 16px solid transparent;
            border-right: 16px solid transparent;
            border-top: 24px solid #1565c0;
            margin: 0 auto;
        }
        .branch {
            display: flex;
            flex-direction: row;
            gap: 80px;
            justify-content: center;
            width: 100%;
            margin: 0;
        }
        .branch-column {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 18px;
        }
        .yes-label, .no-label {
            font-size: 0.95em;
            font-weight: bold;
            color: #1565c0;
            position: absolute;
            top: -22px;
        }
        .yes-label {
            left: 50px;
        }
        .no-label {
            right: 50px;
        }
        @media (max-width: 600px) {
            .container { padding: 10px; }
            .branch { gap: 18px; }
            .step, .decision { min-width: 120px; font-size: .98em; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>E-commerce Order Process Flow</h1>
        <div class="flowchart">

            <div class="start step">Start</div>
            <div class="arrow"></div>

            <div class="step">Browse</div>
            <div class="arrow"></div>
            
            <div class="decision step">Found the Product?</div>
            <div class="branch">
                <div class="branch-column">
                    <span class="no-label">No</span>
                    <div class="step">Search</div>
                    <div class="arrow"></div>
                    <div class="step">Checkout</div>
                    <div class="arrow"></div>
                    <div class="step">Choose mode of payment</div>
                </div>
                <div class="branch-column">
                    <span class="yes-label">Yes</span>
                    <div class="step">Check Details</div>
                    <div class="arrow"></div>
                    <div class="decision step">Satisfied?</div>
                    <div class="branch">
                        <div class="branch-column">
                            <span class="no-label">No</span>
                            <!-- End branch if not satisfied -->
                        </div>
                        <div class="branch-column">
                            <span class="yes-label">Yes</span>
                            <div class="step">Add to Cart</div>
                            <div class="arrow"></div>
                            <div class="step">Place Order</div>
                            <div class="arrow"></div>
                            <div class="step">Email/Notification sent to customer</div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="arrow"></div>
            <div class="step">Sent to warehouse</div>
            <div class="arrow"></div>
            <div class="step">Ship order</div>
            <div class="arrow"></div>
            <div class="step">Receive Order</div>
            <div class="arrow"></div>
            <div class="step">Feedback</div>
            <div class="arrow"></div>
            <div class="end step">End</div>
        </div>
    </div>
</body>
</html>
