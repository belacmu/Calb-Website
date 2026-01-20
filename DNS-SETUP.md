# DNS Configuration for www.calbmusic.com

## Current Status

✅ **GitHub Pages is properly configured and deployed!**

The website is successfully deployed via GitHub Pages workflow. However, your custom domain `www.calbmusic.com` requires DNS configuration at your domain registrar to make it accessible.

## Why the site isn't accessible

The error "www.calbmusic.com's server IP address could not be found" means that the DNS records for your domain are not configured to point to GitHub Pages servers.

## Required DNS Configuration

You need to log in to your domain registrar (where you purchased `calbmusic.com`) and configure the following DNS records:

### Option 1: Using www subdomain (Recommended)

Configure a CNAME record:

| Type   | Name/Host | Value/Points to      | TTL  |
|--------|-----------|---------------------|------|
| CNAME  | www       | belacmu.github.io   | 3600 |

### Option 2: Support both root domain and www subdomain

If you want both `calbmusic.com` and `www.calbmusic.com` to work, configure these records:

**A Records for root domain:**

| Type | Name/Host | Value/Points to   | TTL  |
|------|-----------|------------------|------|
| A    | @         | 185.199.108.153  | 3600 |
| A    | @         | 185.199.109.153  | 3600 |
| A    | @         | 185.199.110.153  | 3600 |
| A    | @         | 185.199.111.153  | 3600 |

**CNAME Record for www:**

| Type   | Name/Host | Value/Points to      | TTL  |
|--------|-----------|---------------------|------|
| CNAME  | www       | belacmu.github.io   | 3600 |

## Steps to Configure DNS

1. **Log in to your domain registrar** (e.g., GoDaddy, Namecheap, Google Domains, etc.)
2. **Navigate to DNS Management** or DNS settings for `calbmusic.com`
3. **Add the CNAME record** as shown in the table above
4. **Save the changes**
5. **Wait for DNS propagation** (can take up to 48 hours, but usually 15-30 minutes)

## Verify DNS Configuration

After configuring DNS, you can verify it's working by:

1. Using online tools like [DNS Checker](https://dnschecker.org/) - enter `www.calbmusic.com`
2. Using command line:
   ```bash
   # Check CNAME record
   nslookup www.calbmusic.com
   
   # Or using dig
   dig www.calbmusic.com
   ```

## What happens after DNS is configured?

Once DNS is properly configured:
- `www.calbmusic.com` will resolve to GitHub Pages servers
- Your website will be accessible at `https://www.calbmusic.com/`
- HTTPS will be automatically enabled by GitHub Pages
- Any pushes to the `main` branch will automatically update your live site

## Troubleshooting

### Site still not accessible after 24+ hours?

1. Verify DNS records are correct using DNS checker tools
2. Clear your browser cache and DNS cache
3. Try accessing from a different network or device
4. Check that you've configured the DNS records at the correct domain registrar

### Getting SSL/HTTPS errors?

1. Go to your GitHub repository settings → Pages
2. Wait for GitHub to provision the SSL certificate (can take a few minutes after DNS is configured)
3. Enable "Enforce HTTPS" option if not already enabled

## Current Deployment Info

- **Repository**: belacmu/Calb-Website
- **Branch**: main
- **Workflow**: Jekyll GitHub Pages deployment
- **Last Deployment**: Successfully deployed to GitHub Pages
- **Target URL**: https://www.calbmusic.com/

## Need Help?

If you're unsure how to configure DNS records:
1. Contact your domain registrar's support team
2. Provide them with the CNAME record details from this document
3. Ask them to configure the DNS records for GitHub Pages

---

**Note**: This repository is already correctly configured for GitHub Pages. No code changes are needed - only DNS configuration at your domain registrar.
