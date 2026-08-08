<div align="center">

# Vũ Văn Hải

**Backend Developer @ CES Global**

Node.js | TypeScript | PostgreSQL | DevOps

Ho Chi Minh City, Vietnam

<a href="https://www.linkedin.com/in/haivv/">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logoColor=white" height="25" alt="linkedin"/>
</a>
<a href="mailto:haivv.se@gmail.com">
  <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" height="25" alt="gmail"/>
</a>
<a href="https://discordapp.com/users/813281719191863366">
  <img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" height="25" alt="discord"/>
</a>
<a href="https://www.facebook.com/VuVanHai.02">
  <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" height="25" alt="facebook"/>
</a>

</div>

---

## About

Backend developer with **2.5 years of experience**, currently at **CES Global**, where I own the entire backend of the company's live CRM and course-commerce platform: **204 endpoints, 42 tables, 17 cron jobs**, serving the internal CRM, a digital document library and ~12 campaign landing pages.

What I actually spend my days on:

- **Third-party integration** - bank-transfer payments, Vietnamese e-invoicing (MISA meInvoice), transactional and marketing email at 11,000+ recipients, OAuth, object storage.
- **Idempotent, concurrency-safe PostgreSQL design** - partial unique indexes as business locks, advisory locks, compare-and-swap over pessimistic locking.
- **Production operations** - cron runners with overlap protection, bank reconciliation, order rescue, bulk imports. Scripts are idempotent, dry-run by default, and back up before writing.
- **Self-managed infrastructure** - 12 Dockerized services on a hardened Ubuntu VPS I secure, back up and monitor myself. Containers run non-root behind host Caddy, with encrypted off-host database backups.
- **AI agent engineering** - I ship agents to production, not demos: self-written agent loops, tool-permission models, layered prompt-injection defense, token budgeting, and evals that run against real models.

Background: .NET / C# / ASP.NET Core / SQL Server. Still fluent, just not where I spend most of my time now.

<details>
<summary><b>Tiếng Việt</b></summary>

<br>

Backend developer với **2.5 năm kinh nghiệm**, hiện làm tại **CES Global**, nơi tôi tự dựng và vận hành **toàn bộ backend** của nền tảng CRM + bán khóa học đang chạy production: **204 endpoint, 42 bảng, 17 cron job**, phục vụ đồng thời CRM nội bộ, thư viện tài liệu số và khoảng 12 landing page bán khóa học.

Những mảng tôi làm hằng ngày:

- **Tích hợp bên thứ ba** - thanh toán chuyển khoản, hóa đơn điện tử (MISA meInvoice), email giao dịch và email marketing quy mô 11.000+ người nhận, OAuth, object storage.
- **Thiết kế PostgreSQL chống trùng và an toàn khi đồng thời** - chỉ mục duy nhất bộ phận làm khóa nghiệp vụ, advisory lock, compare-and-swap thay cho khóa bi quan.
- **Vận hành production** - cron runner có chống chạy đè, đối soát ngân hàng, cứu đơn hàng lỗi, nhập dữ liệu hàng loạt. Script viết theo hướng chạy lại được, mặc định dry-run, sao lưu trước khi ghi.
- **Tự quản hạ tầng** - 12 dịch vụ Docker trên VPS Ubuntu do tôi tự hardening, tự backup, tự giám sát. Container chạy non-root sau Caddy trên host, backup CSDL mã hóa trước khi rời máy.
- **AI agent engineering** - tôi đưa agent ra production chứ không dừng ở demo: agent loop tự viết, mô hình phân quyền công cụ, phòng prompt injection nhiều lớp, quản lý ngân sách token, và bộ eval chạy trên model thật.

Nền tảng cũ: .NET / C# / ASP.NET Core / SQL Server. Vẫn dùng tốt, chỉ là không còn là nơi tôi dành phần lớn thời gian.

</details>

---

## Featured Projects

### [zalo-agent](https://github.com/vuhai2002/zalo-agent) `MIT`

Self-hosted AI agent running in production on a messaging platform. Multi-account in a single process, each with its own persona and tool set.

- Self-written agent loop over the Vercel AI SDK with **13 tools** and **61 dashboard endpoints**
- **Layered prompt-injection defense** for an agent that reads messages from strangers: sanitized untrusted-content boundaries, SSRF guard covering redirect hops and DNS rebinding, output-side system-prompt leak blocking, and deliberately no financial tools
- Real token budgeting after measuring a single turn accumulating 184,835 tokens over 8 steps
- **1,562 tests** on Node's built-in test runner, plus **17 evals that run a real model**
- Provider-agnostic: any OpenAI-compatible endpoint, Anthropic, or Google

`TypeScript` `Vercel AI SDK` `Hono` `React 19` `SQLite` `Docker`

### AI Translator - Chrome Extension `294 users` `5.0 stars`

A three-part system with real users on the [Chrome Web Store](https://chromewebstore.google.com/detail/hkelkkhcmkhbpkenoogdeomannakpilk), maintained for 16 months.

- Hover, selection and context-menu translation across **50+ languages**
- Two translation paths tuned to the speed-versus-quality tradeoff of each interaction
- [Express 5 proxy backend](https://github.com/vuhai2002/translation-server) keeping API keys server-side, with automatic failover to a backup provider and IP + User-Agent rate limiting

[`extension`](https://github.com/vuhai2002/AITranslatorExtension) - [`backend`](https://github.com/vuhai2002/translation-server) - `Manifest V3` `Express 5` `Docker`

### [vietnamese-tts-studio](https://github.com/vuhai2002/vietnamese-tts-studio)

Offline Vietnamese text-to-speech and voice cloning - fully local on your own NVIDIA GPU, works on 4GB VRAM. No internet, no API keys, nothing leaves the machine. Web UI + CLI.

`Python` `PyTorch` `FastAPI` `OmniVoice`

### [developer-handbook](https://github.com/vuhai2002/developer-handbook) `MIT`

A practical handbook of setup guides and production-ready recipes collected from real work: VPS provisioning, Caddy reverse proxy, PostgreSQL tuning and migration, media CDN over Cloudflare + B2, third-party integrations.

### [ai-slides-mcp](https://github.com/vuhai2002/ai-slides-mcp)

MCP server and CLI that generates images and assembles them into full-bleed PowerPoint decks - brand-aware (auto-detects palette from your logo) or styled after a reference image. Works over stdio across Claude Code, Codex and Antigravity.

### [claude-agent-monitor](https://github.com/vuhai2002/claude-agent-monitor)

Zero-dependency localhost dashboard showing which Claude Code subagents are currently running - information the desktop UI does not surface. Node built-ins only.

<details>
<summary><b>Dự án nổi bật (tiếng Việt)</b></summary>

<br>

- **[zalo-agent](https://github.com/vuhai2002/zalo-agent)** `MIT` - AI agent tự host, chạy production trên nền tảng nhắn tin. Nhiều tài khoản trong một tiến trình, mỗi tài khoản một persona riêng. Agent loop tự viết trên Vercel AI SDK, 13 công cụ, 61 endpoint dashboard, phòng prompt injection nhiều lớp, 1.562 test + 17 eval chạy model thật.
- **AI Translator - Chrome Extension** - hệ thống 3 phần có người dùng thật: **294 người dùng, 5.0 sao** trên Chrome Web Store, duy trì 16 tháng. Dịch hover / bôi đen / chuột phải qua 50+ ngôn ngữ, backend proxy Express 5 giữ API key phía server, có fallback tự động.
- **[vietnamese-tts-studio](https://github.com/vuhai2002/vietnamese-tts-studio)** - TTS tiếng Việt và clone giọng chạy offline 100% trên GPU NVIDIA của chính bạn, chỉ cần 4GB VRAM. Không internet, không API key. Có web UI và CLI.
- **[developer-handbook](https://github.com/vuhai2002/developer-handbook)** `MIT` - sổ tay hướng dẫn đúc từ việc thật: dựng VPS, Caddy reverse proxy, tối ưu và migrate PostgreSQL, media CDN qua Cloudflare + B2, tích hợp dịch vụ bên thứ ba.
- **[ai-slides-mcp](https://github.com/vuhai2002/ai-slides-mcp)** - MCP server + CLI sinh ảnh rồi ghép thành slide PowerPoint tràn viền, tự dò bảng màu thương hiệu từ logo hoặc bám theo phong cách một ảnh mẫu. Chạy qua stdio trên Claude Code, Codex, Antigravity.
- **[claude-agent-monitor](https://github.com/vuhai2002/claude-agent-monitor)** - dashboard localhost cho biết subagent nào của Claude Code đang chạy, thứ mà giao diện Desktop không hiển thị. Không cần cài dependency.

</details>

---

## Tech Stack

**Languages**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)

**AI / LLM**

![Vercel AI SDK](https://img.shields.io/badge/Vercel%20AI%20SDK-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-191919?style=for-the-badge&logo=anthropic&logoColor=white)
![OpenAI compatible](https://img.shields.io/badge/OpenAI%20compatible-412991?style=for-the-badge&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=modelcontextprotocol&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Hono](https://img.shields.io/badge/Hono-E36002?style=for-the-badge&logo=hono&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

**Database**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle%20ORM-C5F74F?style=for-the-badge&logo=drizzle&logoColor=black)
![Entity Framework](https://img.shields.io/badge/EF%20Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TanStack](https://img.shields.io/badge/TanStack-FF4154?style=for-the-badge&logo=reactquery&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

**DevOps / Infrastructure**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1F88C0?style=for-the-badge&logo=caddy&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2671E5?style=for-the-badge&logo=githubactions&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0072C6?style=for-the-badge&logoColor=white)

---

<div align="center">

Open to backend and DevOps conversations - reach me on [LinkedIn](https://www.linkedin.com/in/haivv/) or [email](mailto:haivv.se@gmail.com).

</div>
