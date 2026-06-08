
function articleCard(a){
  return `<article class="card article-card">
    <p class="category">${a.category}</p>
    <h3>${a.title}</h3>
    <p>${a.description}</p>
    <small>${a.date}｜${a.read}</small>
    <a href="${a.url}">閱讀文章 →</a>
  </article>`;
}
function renderLatest(){
  const el=document.getElementById("latestArticles");
  if(el) el.innerHTML=ARTICLES.slice(0,6).map(articleCard).join("");
}
function renderArticles(category="全部"){
  const el=document.getElementById("articleList"); if(!el) return;
  const keyword=(document.getElementById("articleSearch")?.value||"").trim();
  let list=ARTICLES;
  if(category!=="全部") list=list.filter(a=>a.category===category);
  if(keyword) list=list.filter(a=>(a.title+a.description+a.category).includes(keyword));
  el.innerHTML=list.map(articleCard).join("") || `<p>目前沒有符合條件的文章。</p>`;
}
function renderPrompts(){
  const el=document.getElementById("promptList"); if(!el) return;
  el.innerHTML=PROMPTS.map((p,i)=>`
    <article class="card prompt-card">
      <h3>${p.title}</h3><p>${p.desc}</p>
      <textarea readonly id="prompt-${i}">${p.prompt}</textarea>
      <button class="btn secondary" onclick="copyPrompt(${i})">複製 Prompt</button>
    </article>`).join("");
}
function copyPrompt(i){
  const el=document.getElementById(`prompt-${i}`);
  navigator.clipboard.writeText(el.value);
  alert("已複製 Prompt");
}
function subscribeDemo(e){
  e.preventDefault();
  document.getElementById("subscribeMsg").textContent="已收到！正式版可串接 Mailchimp、ConvertKit 或後端資料庫。";
}
function calculateCompound(){
  const monthly=Number(document.getElementById("monthly").value);
  const annual=Number(document.getElementById("rate").value)/100;
  const years=Number(document.getElementById("years").value);
  const months=years*12;
  const r=annual/12;
  let total=0;
  for(let i=0;i<months;i++){ total=(total+monthly)*(1+r); }
  const invested=monthly*months;
  const gain=total-invested;
  const fmt=n=>Math.round(n).toLocaleString("zh-TW");
  document.getElementById("result").innerHTML=`
    <h2>試算結果</h2>
    <p>總投入：約 NT$${fmt(invested)}</p>
    <p>預估資產：約 NT$${fmt(total)}</p>
    <p>預估成長：約 NT$${fmt(gain)}</p>
    <p class="lead">提醒：這只是估算，不代表未來一定會達成。</p>`;
}
renderLatest();
renderPrompts();
