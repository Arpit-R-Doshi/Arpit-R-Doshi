```aura width=860 height=200
 <div style={{
 width: '100%', height: '100%', background: '#08080c',
 display: 'flex', alignItems: 'center', fontFamily: 'Manrope',
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
     @keyframes fire-glow {
       0%, 100% { transform: scale(1); opacity: 0.7; }
       50% { transform: scale(1.15); opacity: 1.0; }
     }
     @keyframes fire-flicker {
       0%, 100% { transform: translateY(0px) scale(1); opacity: 0.6; }
       33% { transform: translateY(-8px) scale(1.05); opacity: 0.9; }
       66% { transform: translateY(4px) scale(0.95); opacity: 0.5; }
     }
     @keyframes float-char {
       0%, 100% { transform: translateY(0px); }
       50% { transform: translateY(-8px); }
     }
     #glow-1 { animation: float-slow 8s ease-in-out infinite; }
     #glow-2 { animation: float-medium 12s ease-in-out infinite; }
     #glow-3 { animation: float-fast 9s ease-in-out infinite; }
     #glow-4 { animation: float-slow 11s ease-in-out infinite reverse; }
     #glow-5 { animation: float-medium 14s ease-in-out infinite reverse; }
     #glow-6 { animation: float-diagonal 10s ease-in-out infinite; }
     #glow-7 { animation: float-wave 13s ease-in-out infinite; }
     #glow-8 { animation: float-pulse 7s ease-in-out infinite; }
     #fire-bg-1 { animation: fire-glow 4s ease-in-out infinite; }
     #fire-bg-2 { animation: fire-flicker 3s ease-in-out infinite; }
     #fire-bg-3 { animation: fire-flicker 5s ease-in-out infinite reverse; }
     #char-img { animation: float-char 6s ease-in-out infinite; }
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
     <radialGradient id="fire1" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(255,100,0,0.6)" />
       <stop offset="40%" stopColor="rgba(255,50,0,0.2)" />
       <stop offset="70%" stopColor="rgba(255,0,0,0)" />
     </radialGradient>
     <radialGradient id="fire2" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(255,180,0,0.5)" />
       <stop offset="40%" stopColor="rgba(255,80,0,0.15)" />
       <stop offset="70%" stopColor="rgba(255,0,0,0)" />
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
   
   <ellipse id="fire-bg-1" cx="740" cy="100" rx="220" ry="220" fill="url(#fire1)" />
   <ellipse id="fire-bg-2" cx="680" cy="140" rx="180" ry="180" fill="url(#fire2)" />
   <ellipse id="fire-bg-3" cx="800" cy="80" rx="160" ry="160" fill="url(#fire1)" />
   
   <image id="char-img" href="https://raw.githubusercontent.com/Arpit-R-Doshi/Arpit-R-Doshi/main/Kyojuro_anime.webp" x="600" y="-10" width="220" height="220" preserveAspectRatio="xMidYMid slice" />
 </svg>

 <div style={{ display:'flex', flexDirection:'column', marginLeft:64, gap:8, zIndex: 10 }}>
   <div style={{ display:'flex', fontSize:54, fontWeight:400, color:'#ffffff', letterSpacing:'-1px', lineHeight:1, fontFamily: '"Bebas Neue"' }}>
     Arpit Rajesh Doshi
   </div>
   <div style={{ display:'flex', fontSize:15, color:'rgba(180,165,255,0.8)', fontWeight:400, letterSpacing:'0.3px' }}>
     Systems Software Engineer · Backend & Data Engineer · Web3 Developer
   </div>
 </div>
</div>
```

```aura width=860 height=140
(function() {
 var stats = [
   { label: 'Repos', value: String((github && github.stats && github.stats.totalRepos) || 0), color: '#a78bfa' },
   { label: 'Stars', value: String((github && github.stats && github.stats.totalStars) || 0), color: '#60a5fa' },
   { label: 'Contributions', value: String((github && github.stats && (github.stats.totalContributions || github.stats.contributions || github.stats.totalCommits)) || 0), color: '#f59e0b' },
 ];

 return (
   <div style={{
     width: '100%', height: '100%',
     background: '#08080c',
     display: 'flex', alignItems: 'center', justifyContent: 'center',
     fontFamily: 'Manrope', borderRadius: 16,
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
      fontFamily: 'Manrope', padding: '18px 32px', gap: 14,
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
            <div key={cat.title} style={{ display:'flex', alignItems:'flex-start', gap:16 }}>
              <div style={{ display:'flex', fontSize:10, fontWeight:700, color:cat.color, letterSpacing:'1px', width:130, minWidth:130, marginTop:14 }}>
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
      fontFamily: 'Manrope', padding: '24px 32px', gap: 14,
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

<div align="center">
  
```aura width=130 height=45 inline=true link="https://linkedin.com/in/arpitrajeshdoshi"
(function() {
  return (
    <div style={{
      width: '100%', height: '100%', background: '#000000',
      display: 'flex', alignItems: 'center', justifyContent: 'center', gap: 8,
      fontFamily: 'Manrope', borderRadius: 30, border: '1px solid rgba(0, 119, 181, 0.8)',
      position: 'relative', overflow: 'hidden'
    }}>
      <svg width="100%" height="100%" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="g-in" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(0,119,181,0.5)" />
            <stop offset="100%" stopColor="rgba(0,119,181,0)" />
          </radialGradient>
        </defs>
        <ellipse cx="20%" cy="50%" rx="60%" ry="80%" fill="url(#g-in)" />
        <ellipse cx="80%" cy="50%" rx="60%" ry="80%" fill="url(#g-in)" />
      </svg>
      <div style={{ display: 'flex', alignItems: 'center', gap: 8, zIndex: 10 }}>
        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linkedin/linkedin-original.svg" width={20} height={20} />
        <div style={{ color: '#ffffff', fontSize: 14, fontWeight: 700, letterSpacing: '0.5px' }}>LinkedIn</div>
      </div>
    </div>
  );
})()
```

```aura width=120 height=45 inline=true link="mailto:arpitrajeshdoshi@gmail.com"
(function() {
  return (
    <div style={{
      width: '100%', height: '100%', background: '#000000',
      display: 'flex', alignItems: 'center', justifyContent: 'center', gap: 8,
      fontFamily: 'Manrope', borderRadius: 30, border: '1px solid rgba(234, 67, 53, 0.8)',
      position: 'relative', overflow: 'hidden'
    }}>
      <svg width="100%" height="100%" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="g-mail" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(234,67,53,0.5)" />
            <stop offset="100%" stopColor="rgba(234,67,53,0)" />
          </radialGradient>
        </defs>
        <ellipse cx="20%" cy="50%" rx="60%" ry="80%" fill="url(#g-mail)" />
        <ellipse cx="80%" cy="50%" rx="60%" ry="80%" fill="url(#g-mail)" />
      </svg>
      <div style={{ display: 'flex', alignItems: 'center', gap: 8, zIndex: 10 }}>
        <img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Gmail_icon_%282020%29.svg" width={20} height={20} />
        <div style={{ color: '#ffffff', fontSize: 14, fontWeight: 700, letterSpacing: '0.5px' }}>Email</div>
      </div>
    </div>
  );
})()
```

</div>

<br>
<p align="center"><sub>𝗉𝗈𝗐𝖾𝗋𝖾𝖽 𝖻𝗒 <a href="https://github.com/collectioneur/readme-aura">𝗋𝖾𝖺𝖽𝗆𝖾-𝖺𝗎𝗋𝖺</a></sub></p>
