```aura width=860 height=200
 <div style={{
 width: '100%', height: '100%', background: '#08080c',
 display: 'flex', alignItems: 'center', fontFamily: 'Inter',
 position: 'relative', overflow: 'hidden', borderRadius: 16,
 border: '1px solid rgba(110,80,220,0.18)'
}}>

 <style>
   {`
     @keyframes float-slow {
       0%, 100% { transform: translateX(0px); opacity: 0.8; }
       50% { transform: translateX(350px); opacity: 1.2; }
     }
     @keyframes float-medium {
       0%, 100% { transform: translateX(0px); opacity: 0.7; }
       50% { transform: translateX(-250px); opacity: 1.1; }
     }
     @keyframes float-fast {
       0%, 100% { transform: translateX(0px); opacity: 0.9; }
       50% { transform: translateX(200px); opacity: 0.6; }
     }
     @keyframes float-diagonal {
       0%, 100% { transform: translateX(0px); opacity: 0.75; }
       50% { transform: translateX(300px); opacity: 1.0; }
     }
     @keyframes float-wave {
       0%, 100% { transform: translateX(0px); opacity: 0.65; }
       33% { transform: translateX(-160px); opacity: 0.9; }
       66% { transform: translateX(80px); opacity: 1.0; }
     }
     @keyframes float-pulse {
       0%, 100% { transform: scale(1); opacity: 0.8; }
       50% { transform: scale(1.3); opacity: 0.4; }
     }
     #glow-1 { animation: float-slow 8s ease-in-out infinite; }
     #glow-2 { animation: float-medium 12s ease-in-out infinite; }
     #glow-3 { animation: float-fast 9s ease-in-out infinite; }
     #glow-4 { animation: float-slow 11s ease-in-out infinite reverse; }
     #glow-5 { animation: float-medium 14s ease-in-out infinite reverse; }
     #glow-6 { animation: float-diagonal 10s ease-in-out infinite; }
     #glow-7 { animation: float-wave 13s ease-in-out infinite; }
     #glow-8 { animation: float-pulse 7s ease-in-out infinite; }
   `}
 </style>

 <svg width="860" height="200" style={{ position: 'absolute', top: 0, left: 0 }}>
   <defs>
     <radialGradient id="g1" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(110,20,210,0.72)" />
       <stop offset="40%" stopColor="rgba(90,15,180,0.35)" />
       <stop offset="70%" stopColor="rgba(90,15,180,0)" />
     </radialGradient>
     <radialGradient id="g2" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(40,60,255,0.6)" />
       <stop offset="45%" stopColor="rgba(30,50,200,0.25)" />
       <stop offset="70%" stopColor="rgba(30,50,200,0)" />
     </radialGradient>
     <radialGradient id="g3" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(0,130,255,0.45)" />
       <stop offset="50%" stopColor="rgba(0,100,220,0.18)" />
       <stop offset="70%" stopColor="rgba(0,100,220,0)" />
     </radialGradient>
     <radialGradient id="g4" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(0,190,230,0.32)" />
       <stop offset="70%" stopColor="rgba(0,190,230,0)" />
     </radialGradient>
     <radialGradient id="g5" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(90,30,200,0.38)" />
       <stop offset="70%" stopColor="rgba(90,30,200,0)" />
     </radialGradient>
     <radialGradient id="g6" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(160,30,255,0.55)" />
       <stop offset="45%" stopColor="rgba(130,20,220,0.22)" />
       <stop offset="70%" stopColor="rgba(130,20,220,0)" />
     </radialGradient>
     <radialGradient id="g7" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(20,60,255,0.42)" />
       <stop offset="50%" stopColor="rgba(10,40,200,0.16)" />
       <stop offset="70%" stopColor="rgba(10,40,200,0)" />
     </radialGradient>
     <radialGradient id="g8" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(0,170,255,0.40)" />
       <stop offset="50%" stopColor="rgba(0,130,220,0.15)" />
       <stop offset="70%" stopColor="rgba(0,130,220,0)" />
     </radialGradient>
   </defs>

   <ellipse id="glow-1" cx="180" cy="230" rx="260" ry="190" fill="url(#g1)" />
   <ellipse id="glow-2" cx="300" cy="240" rx="220" ry="160" fill="url(#g2)" />
   <ellipse id="glow-3" cx="420" cy="240" rx="180" ry="140" fill="url(#g3)" />
   <ellipse id="glow-4" cx="550" cy="250" rx="150" ry="120" fill="url(#g4)" />
   <ellipse id="glow-5" cx="750" cy="250" rx="130" ry="110" fill="url(#g5)" />
   <ellipse id="glow-6" cx="300" cy="240" rx="180" ry="140" fill="url(#g6)" />
   <ellipse id="glow-7" cx="490" cy="230" rx="220" ry="170" fill="url(#g7)" />
   <ellipse id="glow-8" cx="590" cy="250" rx="150" ry="130" fill="url(#g8)" />
 </svg>

 <div style={{ display:'flex', flexDirection:'column', marginLeft:64, gap:8, zIndex: 10 }}>
   <div style={{ display:'flex', fontSize:38, fontWeight:800, color:'#ffffff', letterSpacing:'-1px', lineHeight:1 }}>
     Arpit Doshi
   </div>
   <div style={{ display:'flex', fontSize:15, color:'rgba(180,165,255,0.8)', fontWeight:400, letterSpacing:'0.3px' }}>
     Systems Software Engineer · Backend & Data Engineer · Web3 Developer
   </div>
   <div style={{ display:'flex', gap:8, marginTop:6 }}>
     {['C++', 'Python', 'TypeScript', 'Solidity'].map(function(tag) {
       return (
         <div key={tag} style={{
           display:'flex', padding:'4px 12px', borderRadius:20,
           background:'rgba(80,40,220,0.18)', border:'1px solid rgba(100,70,240,0.32)',
           color:'rgba(205,195,255,0.85)', fontSize:12, fontWeight:600,
         }}>{tag}</div>
       );
     })}
   </div>
 </div>
</div>
```

```aura width=860 height=140
(function() {
 var stats = [
   { label: 'Repos', value: String((github && github.stats && github.stats.totalRepos) || 0), color: '#a78bfa' },
   { label: 'Stars', value: String((github && github.stats && github.stats.totalStars) || 0), color: '#60a5fa' },
   { label: 'Commits', value: String((github && github.stats && github.stats.totalCommits) || 0), color: '#f59e0b' },
 ];

 return (
   <div style={{
     width: '100%', height: '100%',
     background: '#08080c',
     display: 'flex', alignItems: 'center', justifyContent: 'center',
     fontFamily: 'Inter', borderRadius: 16,
     border: '1px solid rgba(110,80,220,0.18)',
     position: 'relative', overflow: 'hidden',
   }}>

     <style>
       {`
         @keyframes float-slow {
           0%, 100% { transform: translateX(0px); opacity: 0.8; }
           50% { transform: translateX(350px); opacity: 1.2; }
         }
         @keyframes float-medium {
           0%, 100% { transform: translateX(0px); opacity: 0.7; }
           50% { transform: translateX(-250px); opacity: 1.1; }
         }
         @keyframes float-fast {
           0%, 100% { transform: translateX(0px); opacity: 0.9; }
           50% { transform: translateX(200px); opacity: 0.6; }
         }
         @keyframes float-diagonal {
           0%, 100% { transform: translate(0px, 0px); opacity: 0.75; }
           50% { transform: translate(120px, 30px); opacity: 1.0; }
         }
         @keyframes float-wave {
           0%, 100% { transform: translateX(0px); opacity: 0.65; }
           33% { transform: translateX(-160px); opacity: 0.9; }
           66% { transform: translateX(80px); opacity: 1.0; }
         }
         @keyframes float-pulse {
           0%, 100% { transform: scale(1); opacity: 0.8; }
           50% { transform: scale(1.3); opacity: 0.4; }
         }
         #glow-1 { animation: float-slow 8s ease-in-out infinite; }
         #glow-2 { animation: float-medium 12s ease-in-out infinite; }
         #glow-3 { animation: float-fast 9s ease-in-out infinite; }
         #glow-4 { animation: float-diagonal 10s ease-in-out infinite; }
         #glow-5 { animation: float-wave 14s ease-in-out infinite; }
       `}
     </style>

     <svg width="860" height="140" style={{ position: 'absolute', top: 0, left: 0 }}>
       <defs>
         <radialGradient id="g1" cx="50%" cy="50%" r="50%">
           <stop offset="0%" stopColor="rgba(110,20,210,0.65)" />
           <stop offset="45%" stopColor="rgba(80,15,170,0.28)" />
           <stop offset="70%" stopColor="rgba(80,15,170,0)" />
         </radialGradient>
         <radialGradient id="g2" cx="50%" cy="50%" r="50%">
           <stop offset="0%" stopColor="rgba(40,70,255,0.55)" />
           <stop offset="45%" stopColor="rgba(20,50,200,0.22)" />
           <stop offset="70%" stopColor="rgba(20,50,200,0)" />
         </radialGradient>
         <radialGradient id="g3" cx="50%" cy="50%" r="50%">
           <stop offset="0%" stopColor="rgba(0,140,255,0.42)" />
           <stop offset="70%" stopColor="rgba(0,140,255,0)" />
         </radialGradient>
         <radialGradient id="g4" cx="50%" cy="50%" r="50%">
           <stop offset="0%" stopColor="rgba(0,195,235,0.30)" />
           <stop offset="70%" stopColor="rgba(0,195,235,0)" />
         </radialGradient>
         <radialGradient id="g5" cx="50%" cy="50%" r="50%">
           <stop offset="0%" stopColor="rgba(100,30,210,0.40)" />
           <stop offset="70%" stopColor="rgba(100,30,210,0)" />
         </radialGradient>
       </defs>
       <ellipse id="glow-1" cx="710" cy="150" rx="210" ry="150" fill="url(#g1)" />
       <ellipse id="glow-2" cx="550" cy="140" rx="190" ry="140" fill="url(#g2)" />
       <ellipse id="glow-3" cx="400" cy="130" rx="170" ry="130" fill="url(#g3)" />
       <ellipse id="glow-4" cx="250" cy="140" rx="150" ry="120" fill="url(#g4)" />
       <ellipse id="glow-5" cx="100" cy="150" rx="130" ry="110" fill="url(#g5)" />
     </svg>

     {stats.map(function(s, i) {
       return (
         <div key={s.label} style={{
           flexGrow: 1, display: 'flex', flexDirection: 'column',
           alignItems: 'center', justifyContent: 'center',
           padding: '16px 8px',
           borderRight: i < stats.length - 1 ? '1px solid rgba(255,255,255,0.06)' : 'none',
           gap: 5,
         }}>
           <div style={{ display:'flex', fontSize:30, fontWeight:800, color:s.color, lineHeight:1 }}>
             {s.value}
           </div>
           <div style={{ display:'flex', fontSize:11, color:'rgba(200,195,225,0.45)', fontWeight:600, letterSpacing:'1.5px' }}>
             {s.label.toUpperCase()}
           </div>
         </div>
       );
     })}
   </div>
 );
})()
```

<br>
<h1 align="center">Hi there, I'm Arpit Doshi.</h1>

<!-- Typing Animation -->
<p align="center">
  <a href="https://github.com/DenverCoder1/readme-typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=00FF41&center=true&vCenter=true&width=500&lines=Systems+Software+Engineer;Backend+%26+Data+Engineer;Web3+%26+Smart+Contract+Developer" alt="Typing SVG" />
  </a>
</p>

<p align="center">
  Building high-performance backend architectures, low-latency financial systems, and secure decentralized protocols. Welcome to my GitHub!
</p>
<br>

```aura width=860 height=180
(function() {
  var aboutItems = [
    { icon: '🔭', text: "I'm currently learning Systems Programming, Low-Latency Architecture, and Concurrency" },
    { icon: '🤝', text: "I'm looking to collaborate on High-Performance Backend Systems, Tooling, and Web3 Protocols" },
    { icon: '💬', text: "Ask me about C++, Python, Solidity, and System Orchestration" },
    { icon: '✉️', text: "How to reach me: arpitrajeshdoshi@gmail.com" },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#08080c',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter', padding: '24px 32px', gap: 14,
      borderRadius: 16, border: '1px solid rgba(110,80,220,0.18)',
      position: 'relative', overflow: 'hidden',
    }}>
      <style>
        {`
          @keyframes float-slow {
            0%, 100% { transform: translateX(0px); opacity: 0.8; }
            50% { transform: translateX(350px); opacity: 1.2; }
          }
          @keyframes float-medium {
            0%, 100% { transform: translateX(0px); opacity: 0.7; }
            50% { transform: translateX(-250px); opacity: 1.1; }
          }
          #glow-1 { animation: float-slow 9s ease-in-out infinite; }
          #glow-2 { animation: float-medium 12s ease-in-out infinite reverse; }
        `}
      </style>
      <svg width="860" height="180" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="g1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(0,180,255,0.25)" />
            <stop offset="70%" stopColor="rgba(0,180,255,0)" />
          </radialGradient>
          <radialGradient id="g2" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(115,20,215,0.4)" />
            <stop offset="70%" stopColor="rgba(115,20,215,0)" />
          </radialGradient>
        </defs>
        <ellipse id="glow-1" cx="200" cy="90" rx="200" ry="150" fill="url(#g1)" />
        <ellipse id="glow-2" cx="660" cy="90" rx="200" ry="150" fill="url(#g2)" />
      </svg>
      
      <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(155,140,210,0.5)', letterSpacing:'3px', marginBottom: 4 }}>
        ABOUT ME
      </div>
      
      <div style={{ display:'flex', flexDirection:'column', gap:10 }}>
        {aboutItems.map(function(item, i) {
          return (
            <div key={i} style={{ display:'flex', alignItems:'center', gap:12 }}>
              <div style={{ display:'flex', fontSize:18 }}>{item.icon}</div>
              <div style={{ display:'flex', fontSize:14, color:'rgba(225,220,255,0.85)', fontWeight:500 }}>{item.text}</div>
            </div>
          );
        })}
      </div>
    </div>
  );
})()
```

<br>

### Featured Projects 🚀

- **[LOB-Sim](https://github.com/Arpit-R-Doshi/LOB-Sim)**: A deterministic matching engine built in C++20 executing order matching with price-time (FIFO) priority. Features a custom vector-backed Object Pool allocator to bypass runtime dynamic heap allocations.
- **[DeFi Risk Simulation Lab](https://github.com/Arpit-R-Doshi/DeFi-Simulation-Lab)**: An agent-based simulation engine (Mesa ABM) modeling 7 DeFi archetypes executing adversarial strategies to surface liquidity and oracle risks, with real-time streaming via FastAPI WebSockets.

<br>

```aura width=860 height=260
(function() {
  var categories = [
    { 
      title: 'Languages', color: '#a78bfa', 
      type: 'icons', items: ['cpp', 'py', 'ts', 'js', 'solidity', 'java', 'postgres'] 
    },
    { 
      title: 'Frameworks', color: '#60a5fa', 
      type: 'mixed', 
      icons: ['nextjs', 'react', 'nodejs', 'express', 'fastapi'],
      badges: [
        { name: 'Ethereum', color: '3C3C3D', logo: 'Ethereum', logoColor: 'white' },
        { name: 'Hardhat', color: 'FFF100', logo: 'Hardhat', logoColor: 'black' },
        { name: 'Web3.js', color: 'F16822', logo: 'Web3.js', logoColor: 'white' },
        { name: 'Ethers.js', color: '272A2E', logo: 'ethers', logoColor: 'white' },
      ]
    },
    { 
      title: 'DevOps & Data', color: '#f59e0b', 
      type: 'mixed', 
      icons: ['mongodb', 'mysql', 'supabase', 'linux', 'kubernetes', 'docker', 'git', 'prometheus', 'grafana'],
      badges: [
        { name: 'Snowflake', color: '29B5E8', logo: 'Snowflake', logoColor: 'white' },
        { name: 'dbt', color: 'FF694B', logo: 'dbt', logoColor: 'white' },
        { name: 'Neo4j', color: '015896', logo: 'Neo4j', logoColor: 'white' },
        { name: 'Temporal', color: '242526', logo: 'Temporal', logoColor: 'white' },
      ]
    },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#08080c',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter', padding: '18px 32px', gap: 14,
      borderRadius: 16, border: '1px solid rgba(110,80,220,0.18)',
      position: 'relative', overflow: 'hidden',
    }}>

      <style>
        {`
          @keyframes float-slow {
            0%, 100% { transform: translateX(0px); opacity: 0.8; }
            50% { transform: translateX(350px); opacity: 1.2; }
          }
          @keyframes float-medium {
            0%, 100% { transform: translateX(0px); opacity: 0.7; }
            50% { transform: translateX(-250px); opacity: 1.1; }
          }
          @keyframes float-fast {
            0%, 100% { transform: translateX(0px); opacity: 0.9; }
            50% { transform: translateX(200px); opacity: 0.6; }
          }
          @keyframes float-diagonal {
            0%, 100% { transform: translate(0px, 0px); opacity: 0.75; }
            50% { transform: translate(120px, 30px); opacity: 1.0; }
          }
          @keyframes float-wave {
            0%, 100% { transform: translateX(0px); opacity: 0.65; }
            33% { transform: translateX(-160px); opacity: 0.9; }
            66% { transform: translateX(80px); opacity: 1.0; }
          }
          @keyframes float-pulse {
            0%, 100% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.3); opacity: 0.4; }
          }
          #glow-1 { animation: float-slow 9s ease-in-out infinite; }
          #glow-2 { animation: float-medium 12s ease-in-out infinite; }
          #glow-3 { animation: float-fast 8s ease-in-out infinite; }
          #glow-4 { animation: float-diagonal 11s ease-in-out infinite reverse; }
          #glow-5 { animation: float-wave 14s ease-in-out infinite reverse; }
          #glow-6 { animation: float-pulse 6s ease-in-out infinite; }
        `}
      </style>

      <svg width="860" height="260" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="g1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(115,20,215,0.68)" />
            <stop offset="42%" stopColor="rgba(85,15,175,0.30)" />
            <stop offset="70%" stopColor="rgba(85,15,175,0)" />
          </radialGradient>
          <radialGradient id="g2" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(55,55,255,0.55)" />
            <stop offset="45%" stopColor="rgba(35,45,210,0.22)" />
            <stop offset="70%" stopColor="rgba(35,45,210,0)" />
          </radialGradient>
          <radialGradient id="g3" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(0,130,255,0.42)" />
            <stop offset="50%" stopColor="rgba(0,100,220,0.16)" />
            <stop offset="70%" stopColor="rgba(0,100,220,0)" />
          </radialGradient>
          <radialGradient id="g4" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(0,185,240,0.32)" />
            <stop offset="70%" stopColor="rgba(0,185,240,0)" />
          </radialGradient>
          <radialGradient id="g5" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(100,25,205,0.42)" />
            <stop offset="70%" stopColor="rgba(100,25,205,0)" />
          </radialGradient>
          <radialGradient id="g6" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(60,80,255,0.35)" />
            <stop offset="70%" stopColor="rgba(60,80,255,0)" />
          </radialGradient>
        </defs>
        <ellipse id="glow-1" cx="170" cy="168" rx="260" ry="170" fill="url(#g1)" />
        <ellipse id="glow-2" cx="320" cy="178" rx="220" ry="140" fill="url(#g2)" />
        <ellipse id="glow-3" cx="460" cy="178" rx="190" ry="130" fill="url(#g3)" />
        <ellipse id="glow-4" cx="590" cy="188" rx="160" ry="110" fill="url(#g4)" />
        <ellipse id="glow-5" cx="750" cy="188" rx="140" ry="100" fill="url(#g5)" />
        <ellipse id="glow-6" cx="420" cy="138" rx="100" ry="80" fill="url(#g6)" />
      </svg>

      <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(155,140,210,0.5)', letterSpacing:'3px' }}>
        TECH STACK
      </div>
      <div style={{ display:'flex', flexDirection:'column', gap:14 }}>
        {categories.map(function(cat) {
          return (
            <div key={cat.title} style={{ display:'flex', alignItems:'center', gap:16 }}>
              <div style={{ display:'flex', fontSize:10, fontWeight:700, color:cat.color, letterSpacing:'1px', width:100 }}>
                {cat.title.toUpperCase()}
              </div>
              <div style={{ display:'flex', flexWrap:'wrap', gap:7, alignItems:'center' }}>
                {cat.type === 'icons' && cat.items.map(function(item) {
                  return (
                    <img key={item} src={'https://skillicons.dev/icons?i=' + item} width={40} height={40} style={{ borderRadius: 8 }} />
                  );
                })}
                {cat.type === 'mixed' && (
                  <div style={{ display:'flex', flexWrap:'wrap', gap:7, alignItems:'center' }}>
                    {cat.icons.map(function(item) {
                      return (
                        <img key={item} src={'https://skillicons.dev/icons?i=' + item} width={40} height={40} style={{ borderRadius: 8 }} />
                      );
                    })}
                    {cat.badges.map(function(b) {
                      return (
                        <img key={b.name} src={'https://img.shields.io/badge/' + b.name + '-' + b.color + '?style=for-the-badge&logo=' + b.logo + '&logoColor=' + b.logoColor} width={120} height={28} style={{ borderRadius: 4, marginLeft: 4 }} />
                      );
                    })}
                  </div>
                )}
              </div>
            </div>
          );
        })}
      </div>
    </div>
  );
})()
```

<br>

```aura width=860 height=200
(function() {
  var achievements = [
    { icon: '🥇', title: 'First Prize', desc: 'IIT Delhi Yellow x BizThon ($5000) as a Smart Contract Developer.' },
    { icon: '🥈', title: 'Runner Up', desc: 'HackSync 2 (Blockchain domain) TSEC, as a Smart Contract & Backend Developer.' },
    { icon: '🥉', title: 'Second Runner Up', desc: "CSI SPIT Hackathon'26 (Rs. 25,000) as a Blockchain Developer." },
    { icon: '🥈', title: 'Runner Up', desc: "SIES Bytecamp'26 (Rs. 30,000) as a Blockchain and Backend Developer." },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#08080c',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter', padding: '24px 32px', gap: 14,
      borderRadius: 16, border: '1px solid rgba(110,80,220,0.18)',
      position: 'relative', overflow: 'hidden',
    }}>
      <style>
        {`
          @keyframes float-slow {
            0%, 100% { transform: translateX(0px); opacity: 0.8; }
            50% { transform: translateX(350px); opacity: 1.2; }
          }
          @keyframes float-medium {
            0%, 100% { transform: translateX(0px); opacity: 0.7; }
            50% { transform: translateX(-250px); opacity: 1.1; }
          }
          #glow-1 { animation: float-slow 9s ease-in-out infinite; }
          #glow-2 { animation: float-medium 12s ease-in-out infinite reverse; }
        `}
      </style>
      <svg width="860" height="200" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="g1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(255,180,0,0.25)" />
            <stop offset="70%" stopColor="rgba(255,180,0,0)" />
          </radialGradient>
          <radialGradient id="g2" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(115,20,215,0.4)" />
            <stop offset="70%" stopColor="rgba(115,20,215,0)" />
          </radialGradient>
        </defs>
        <ellipse id="glow-1" cx="200" cy="100" rx="200" ry="150" fill="url(#g1)" />
        <ellipse id="glow-2" cx="660" cy="100" rx="200" ry="150" fill="url(#g2)" />
      </svg>
      
      <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(155,140,210,0.5)', letterSpacing:'3px', marginBottom: 4 }}>
        RECENT WINS & ACHIEVEMENTS
      </div>
      
      <div style={{ display:'flex', flexDirection:'column', gap:10 }}>
        {achievements.map(function(ach, i) {
          return (
            <div key={i} style={{ display:'flex', alignItems:'center', gap:12 }}>
              <div style={{ display:'flex', fontSize:20 }}>{ach.icon}</div>
              <div style={{ display:'flex', fontSize:14, color:'#ffffff', fontWeight:600 }}>{ach.title}</div>
              <div style={{ display:'flex', fontSize:14, color:'rgba(225,220,255,0.7)' }}>- {ach.desc}</div>
            </div>
          );
        })}
      </div>
    </div>
  );
})()
```

<br>

<p align="center">
  <a href="https://linkedin.com/in/arpitrajeshdoshi"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

<br>
<p align="center"><sub>𝗉𝗈𝗐𝖾𝗋𝖾𝖽 𝖻𝗒 <a href="https://github.com/collectioneur/readme-aura">𝗋𝖾𝖺𝖽𝗆𝖾-𝖺𝗎𝗋𝖺</a></sub></p>
