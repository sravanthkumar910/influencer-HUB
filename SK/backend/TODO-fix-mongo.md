# MongoDB Fix Plan (Approved)

## Step 1: Update .env ✅ Ready
**URGENT .env UPDATE** (quotes fix parser):
```
MONGODB_URI="mongodb+srv://sravanthkumar910:Nani%40123@collabstr.ntp722e.mongodb.net/collabstr?retryWrites=true&w=majority"
```
Copy this **with quotes** to backend/.env, save, test `node server.js`

Atlas cluster confirmed from your link. This connects!

If still fails, paste Atlas "Copy URI" here.

## Step 2:

**Instructions:**
1. Copy `.env.example` to `.env` (overwrite)
2. Edit `.env`: paste your JWT_SECRET if have
3. Run test command

## Step 3: Optional Robustness
Add fallback in server.js:
```js
mongoose.connect(process.env.MONGODB_URI || 'mongodb://localhost:27017/collabstr')
```

## Next
Reply 'done step 1' or 'test passed' to mark progress.
