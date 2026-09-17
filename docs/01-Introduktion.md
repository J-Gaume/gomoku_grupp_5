## Introduktion till Gomoku

### **Syfte**
- Detta repository är kopplat till kurs för kravhantering
- Repository genomförs i grupp, se [medlemmar :)](https://github.com/johangaume2001-dev/Grupp-5-ovning/graphs/contributors?from=2026-05-30)
- Ingen kod finns då spelet ej skapas
- Övning på kodnära dokumentation i git bash, .md filer, vim text editor och github

### **Spelregler**

1. Spelet består av två spelare
2. Brädan ska vara 15x15 rutor.
3. Vardera spelare placerar en pjäs under sin omgång
4. Man får ej placera en pjäs på upptagen ruta.
5. Fem pjäser i rad, diagonellt/horizontell/vertikalt leder till vinst.
```html
<svg width="680" height="680" viewBox="0 0 680 680" xmlns="http://www.w3.org/2000/svg" role="img">
<title>Gomokubräda 15x15</title>
<desc>En gomokubräda i trä med 15x15 skärningspunkter, med några svarta och vita spelpjäser placerade nära mitten.</desc>
<rect x="10" y="10" width="660" height="660" rx="16" fill="#8b5a2b"/>
<rect x="30" y="30" width="620" height="620" rx="8" fill="#deb887"/>
<g stroke="#5c3a21" stroke-width="1.2">
<line x1="40" y1="40" x2="40" y2="640"/><line x1="82.9" y1="40" x2="82.9" y2="640"/><line x1="125.7" y1="40" x2="125.7" y2="640"/><line x1="168.6" y1="40" x2="168.6" y2="640"/><line x1="211.4" y1="40" x2="211.4" y2="640"/><line x1="254.3" y1="40" x2="254.3" y2="640"/><line x1="297.1" y1="40" x2="297.1" y2="640"/><line x1="340" y1="40" x2="340" y2="640"/><line x1="382.9" y1="40" x2="382.9" y2="640"/><line x1="425.7" y1="40" x2="425.7" y2="640"/><line x1="468.6" y1="40" x2="468.6" y2="640"/><line x1="511.4" y1="40" x2="511.4" y2="640"/><line x1="554.3" y1="40" x2="554.3" y2="640"/><line x1="597.1" y1="40" x2="597.1" y2="640"/><line x1="640" y1="40" x2="640" y2="640"/>
<line x1="40" y1="40" x2="640" y2="40"/><line x1="40" y1="82.9" x2="640" y2="82.9"/><line x1="40" y1="125.7" x2="640" y2="125.7"/><line x1="40" y1="168.6" x2="640" y2="168.6"/><line x1="40" y1="211.4" x2="640" y2="211.4"/><line x1="40" y1="254.3" x2="640" y2="254.3"/><line x1="40" y1="297.1" x2="640" y2="297.1"/><line x1="40" y1="340" x2="640" y2="340"/><line x1="40" y1="382.9" x2="640" y2="382.9"/><line x1="40" y1="425.7" x2="640" y2="425.7"/><line x1="40" y1="468.6" x2="640" y2="468.6"/><line x1="40" y1="511.4" x2="640" y2="511.4"/><line x1="40" y1="554.3" x2="640" y2="554.3"/><line x1="40" y1="597.1" x2="640" y2="597.1"/><line x1="40" y1="640" x2="640" y2="640"/>
</g>
<g fill="#5c3a21">
<circle cx="168.6" cy="168.6" r="4"/><circle cx="168.6" cy="511.4" r="4"/><circle cx="511.4" cy="168.6" r="4"/><circle cx="511.4" cy="511.4" r="4"/><circle cx="340" cy="340" r="4"/>
</g>
<g>
<circle cx="340" cy="340" r="18" fill="#1c1c1c" stroke="#000000" stroke-width="1"/>
<circle cx="334" cy="334" r="5" fill="#5a5a5a" opacity="0.5"/>
<circle cx="340" cy="382.9" r="18" fill="#1c1c1c" stroke="#000000" stroke-width="1"/>
<circle cx="334" cy="376.9" r="5" fill="#5a5a5a" opacity="0.5"/>
<circle cx="382.9" cy="340" r="18" fill="#1c1c1c" stroke="#000000" stroke-width="1"/>
<circle cx="376.9" cy="334" r="5" fill="#5a5a5a" opacity="0.5"/>
<circle cx="297.1" cy="425.7" r="18" fill="#1c1c1c" stroke="#000000" stroke-width="1"/>
<circle cx="291.1" cy="419.7" r="5" fill="#5a5a5a" opacity="0.5"/>
<circle cx="425.7" cy="297.1" r="18" fill="#1c1c1c" stroke="#000000" stroke-width="1"/>
<circle cx="419.7" cy="291.1" r="5" fill="#5a5a5a" opacity="0.5"/>
</g>
<g>
<circle cx="382.9" cy="382.9" r="18" fill="#f7f3ea" stroke="#333333" stroke-width="1.2"/>
<circle cx="376.9" cy="376.9" r="5" fill="#ffffff" opacity="0.7"/>
<circle cx="297.1" cy="340" r="18" fill="#f7f3ea" stroke="#333333" stroke-width="1.2"/>
<circle cx="291.1" cy="334" r="5" fill="#ffffff" opacity="0.7"/>
<circle cx="382.9" cy="297.1" r="18" fill="#f7f3ea" stroke="#333333" stroke-width="1.2"/>
<circle cx="376.9" cy="291.1" r="5" fill="#ffffff" opacity="0.7"/>
<circle cx="254.3" cy="382.9" r="18" fill="#f7f3ea" stroke="#333333" stroke-width="1.2"/>
<circle cx="248.3" cy="376.9" r="5" fill="#ffffff" opacity="0.7"/>
<circle cx="425.7" cy="425.7" r="18" fill="#f7f3ea" stroke="#333333" stroke-width="1.2"/>
<circle cx="419.7" cy="419.7" r="5" fill="#ffffff" opacity="0.7"/>
</g>
</svg>
```
### **Repository struktur**
- Vi har tagit inspiration från olika större projekt där vi valt relevanta filer.
- Dom vi ansåg relevanta till vårat testprojekt om Gomoku valde vi.
