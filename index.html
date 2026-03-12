<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LabInfo OS - Professional Edition</title>
    <style>
        :root {
            --primary: #00d4ff; --secondary: #0055ff; --dark: #020617; 
            --surface: #0f172a; --text: #f1f5f9; --success: #10b981;
            --danger: #ef4444; --warning: #f59e0b;
        }

        body { margin: 0; font-family: 'Segoe UI', sans-serif; background: var(--dark); color: var(--text); overflow: hidden; }
        .hidden { display: none !important; }
        .glass { background: rgba(15, 23, 42, 0.9); backdrop-filter: blur(15px); border: 1px solid rgba(255,255,255,0.1); border-radius: 12px; }

        /* Estilos de Interface */
        .navbar { height: 60px; display: flex; justify-content: space-between; padding: 0 30px; background: rgba(0,0,0,0.9); border-bottom: 1px solid var(--primary); align-items: center; }
        .main-container { display: flex; height: calc(100vh - 60px); }
        .sidebar { width: 260px; padding: 20px; border-right: 1px solid rgba(255,255,255,0.1); overflow-y: auto; }
        .content { flex: 1; padding: 30px; overflow-y: auto; }

        .menu-item { padding: 12px 15px; cursor: pointer; border-radius: 8px; margin-bottom: 8px; color: #94a3b8; transition: 0.3s; }
        .menu-item:hover { background: rgba(0, 212, 255, 0.1); color: var(--primary); }
        .menu-item.active { background: var(--primary); color: #000; font-weight: bold; }
        
        .card { padding: 20px; margin-bottom: 25px; border: 1px solid rgba(255,255,255,0.05); }
        table { width: 100%; border-collapse: collapse; font-size: 0.85rem; }
        th { background: rgba(0, 212, 255, 0.1); color: var(--primary); padding: 12px; text-align: left; }
        td { padding: 12px; border-bottom: 1px solid #1e293b; }
        
        input, select, textarea { background: #020617; color: white; border: 1px solid #334155; padding: 12px; border-radius: 6px; width: 100%; margin-bottom: 10px; box-sizing: border-box; }
        .btn { padding: 8px 15px; border: none; border-radius: 6px; cursor: pointer; font-weight: bold; transition: 0.2s; font-size: 0.8rem; }
        .btn-primary { background: var(--primary); color: #020617; }
        .btn-danger { background: var(--danger); color: white; }
        .btn-pdf { background: #5865f2; color: white; margin-bottom: 15px; }

        /* PCs */
        .pc-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 15px; }
        .pc-item { padding: 20px; text-align: center; border: 2px solid #334155; border-radius: 12px; cursor: pointer; background: rgba(255,255,255,0.02); }
        .pc-item.free { border-color: var(--success); }
        .pc-item.busy { border-color: var(--warning); background: rgba(245, 158, 11, 0.1); }
        .pc-item.maint { border-color: var(--danger); }

        /* Frequência */
        .freq-row { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 10px; }
        .month-box { min-width: 90px; border: 1px solid #334155; padding: 8px; border-radius: 8px; text-align: center; background: #020617; }
        .wk-btn { width: 22px; height: 22px; border-radius: 4px; display: inline-flex; align-items: center; justify-content: center; font-size: 0.7rem; cursor: pointer; margin: 2px; }
        .p-bg { background: var(--success); } .f-bg { background: var(--danger); } .fj-bg { background: var(--warning); color: #000; }

        /* Login */
        .login-screen { height: 100vh; display: flex; align-items: center; justify-content: center; background: radial-gradient(circle, #1e293b 0%, #020617 100%); position: fixed; width: 100%; z-index: 9999; }
        .login-card { padding: 40px; width: 380px; text-align: center; border-bottom: 4px solid var(--primary); }

        /* CONFIGURAÇÃO DE IMPRESSÃO (PDF) */
        @media print {
            body { background: white !important; color: black !important; overflow: visible !important; }
            .no-print, .sidebar, .navbar, .btn, .btn-primary, .btn-danger, input, select { display: none !important; }
            .content { padding: 0 !important; margin: 0 !important; width: 100% !important; }
            .tab-view { display: block !important; } 
            .hidden { display: none !important; }
            .glass { background: transparent !important; border: 1px solid #ccc !important; box-shadow: none !important; }
            table { border: 1px solid black !important; }
            th { background: #eee !important; color: black !important; border: 1px solid black !important; }
            td { border: 1px solid black !important; color: black !important; }
            h2, h3 { color: black !important; text-align: center; margin-bottom: 20px; }
        }
    </style>
</head>
<body>

    <div id="view-login" class="login-screen">
        <div class="login-card glass">
            <h1 style="color: var(--primary);">LABINFO OS</h1>
            <input type="text" id="l-user" placeholder="Usuário">
            <input type="password" id="l-pass" placeholder="Senha">
            <select id="l-role">
                <option value="aluno">Aluno</option>
                <option value="professor">Professor</option>
                <option value="secretaria">Secretaria</option>
                <option value="admin">Administrador</option>
            </select>
            <button class="btn btn-primary" style="width: 100%; margin-top: 15px;" onclick="autenticar()">ENTRAR</button>
        </div>
    </div>

    <nav class="navbar no-print">
        <div><b style="color: var(--primary);">ESTAÇÃO:</b> <span id="display-user">---</span></div>
        <button class="btn btn-danger" onclick="location.reload()">SAIR</button>
    </nav>

    <div class="main-container">
        <aside class="sidebar glass no-print" id="sidebar-menu"></aside>

        <main class="content" id="print-area">
            <div id="tab-dash" class="tab-view">
                <h2 class="no-print">🛰️ Dashboard</h2>
                <div class="card glass no-print" id="mural-view" style="border-left: 5px solid var(--warning); text-align: center;">---</div>
                <div class="no-print" style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin-top: 20px;">
                    <div class="card glass"><h4>Alunos</h4><h2 id="st-alunos">0</h2></div>
                    <div class="card glass"><h4>PCs Livres</h4><h2 id="st-pcs">0/8</h2></div>
                    <div class="card glass"><h4>Formados</h4><h2 id="st-form">0</h2></div>
                </div>
                <div class="card glass no-print">
                    <h3>📚 Cursos Disponíveis</h3>
                    <div id="vitrine-area" style="display: flex; gap: 10px; flex-wrap: wrap;"></div>
                </div>
            </div>

            <div id="tab-matricula" class="tab-view hidden">
                <div class="card glass no-print">
                    <h3>📝 Nova Matrícula</h3>
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
                        <input type="text" id="m-nome" placeholder="Nome Completo">
                        <input type="text" id="m-curso" placeholder="Curso">
                        <input type="text" id="m-user" placeholder="Login">
                        <input type="text" id="m-pass" placeholder="Senha" value="123">
                        <input type="text" id="m-tel" placeholder="Telefone">
                        <input type="text" id="m-resp" placeholder="Responsável">
                        <input type="text" id="m-end" placeholder="Endereço Completo" style="grid-column: span 2;">
                    </div>
                    <button class="btn btn-primary" onclick="cadastrarAluno()">MATRICULAR</button>
                </div>
                
                <div class="card glass">
                    <div style="display: flex; justify-content: space-between; align-items: center;">
                        <h3>📋 Relatório de Alunos Ativos</h3>
                        <button class="btn btn-pdf no-print" onclick="window.print()">📥 Baixar PDF / Imprimir</button>
                    </div>
                    <table id="table-print">
                        <thead>
                            <tr>
                                <th>Aluno</th>
                                <th>Curso</th>
                                <th>Endereço</th>
                                <th>Telefone</th>
                                <th>Responsável</th>
                                <th class="no-print">Login/Senha</th>
                                <th class="no-print">Ações</th>
                            </tr>
                        </thead>
                        <tbody id="list-alunos"></tbody>
                    </table>
                </div>
            </div>

            <div id="tab-frequencia" class="tab-view hidden">
                <h3>📅 Frequência Escolar</h3>
                <div id="freq-area"></div>
            </div>

            <div id="tab-lab" class="tab-view hidden">
                <h3>🖥️ Laboratório</h3>
                <p class="no-print">Clique em um PC para alterar o status (Livre, Reservado ou Manutenção).</p>
                <div class="pc-grid no-print" id="pc-grid-view"></div>
                <div id="pc-edit-card" class="card glass hidden no-print" style="margin-top: 20px;">
                    <h4 id="pc-title-edit">Configurar PC</h4>
                    <label>Informações / Quem Reservou:</label>
                    <textarea id="pc-info-text"></textarea>
                    <label>Status da Máquina:</label>
                    <select id="pc-status-sel">
                        <option value="free">Livre / Disponível</option>
                        <option value="busy">Reservado / Em Uso</option>
                        <option value="maint">Manutenção / Defeito</option>
                    </select>
                    <button class="btn btn-primary" onclick="salvarPC()">SALVAR STATUS</button>
                </div>
            </div>

            <div id="tab-formados" class="tab-view hidden">
                <div class="card glass">
                    <div style="display: flex; justify-content: space-between; align-items: center;">
                        <h3>🎓 Relatório de Formados</h3>
                        <button class="btn btn-pdf no-print" onclick="window.print()">📥 Baixar PDF / Imprimir</button>
                    </div>
                    <table>
                        <thead><tr><th>Nome</th><th>Curso</th><th class="no-print">Ações</th></tr></thead>
                        <tbody id="list-formados"></tbody>
                    </table>
                </div>
            </div>

            <div id="tab-config" class="tab-view hidden">
                <div class="card glass">
                    <h3>👥 Funcionários</h3>
                    <div style="display: flex; gap: 10px;">
                        <input type="text" id="f-user" placeholder="Login">
                        <input type="text" id="f-pass" placeholder="Senha">
                        <select id="f-role"><option value="professor">Professor</option><option value="secretaria">Secretaria</option></select>
                        <button class="btn btn-primary" onclick="addFuncionario()">ADICIONAR</button>
                    </div>
                    <table style="margin-top: 15px;">
                        <thead><tr><th>Usuário</th><th>Senha</th><th>Cargo</th><th>Ação</th></tr></thead>
                        <tbody id="list-func"></tbody>
                    </table>
                </div>
                <div class="card glass">
                    <h3>📚 Vitrine de Cursos</h3>
                    <div style="display: flex; gap: 10px;">
                        <input type="text" id="new-course" placeholder="Nome do Curso">
                        <button class="btn btn-primary" onclick="addCourseVitrine()">CADASTRAR</button>
                    </div>
                    <div id="vitrine-edit-list" style="margin-top: 15px;"></div>
                </div>
            </div>

            <div id="tab-aluno" class="tab-view hidden">
                <div class="card glass">
                    <h2 id="al-nome-display">---</h2>
                    <h4 id="al-curso-display">---</h4>
                    <hr>
                    <div id="al-freq-display"></div>
                </div>
            </div>
        </main>
    </div>

    <script>
        const MESES = ["Jan", "Fev", "Mar", "Abr", "Mai", "Jun", "Jul", "Ago", "Set", "Out", "Nov", "Dez"];
        let db = JSON.parse(localStorage.getItem('labinfo_v6_pdf')) || {
            admin: { user: 'admin', pass: '123' },
            funcionarios: [], alunos: [], formados: [], vitrine: ['Informática'],
            pcs: Array.from({length: 8}, (_, i) => ({id: i+1, status: 'free', info: 'OK'})),
            mural: 'LabInfo OS - Pronto para gerenciar e reservar PCs!'
        };

        let sessao = null;
        let pcAtivoId = null;

        function autenticar() {
            const u = document.getElementById('l-user').value, p = document.getElementById('l-pass').value, r = document.getElementById('l-role').value;
            if(r === 'admin' && u === db.admin.user && p === db.admin.pass) logar('admin', db.admin);
            else if(r === 'aluno') { const a = db.alunos.find(x => x.user === u && x.pass === p); if(a) logar('aluno', a); else alert("Erro!"); }
            else { const f = db.funcionarios.find(x => x.user === u && x.pass === p && x.role === r); if(f) logar(r, f); else alert("Erro!"); }
        }

        function logar(role, dados) {
            sessao = { role, ...dados };
            document.getElementById('view-login').classList.add('hidden');
            document.getElementById('display-user').innerText = (dados.nome || dados.user).toUpperCase();
            montarMenu(); showTab('tab-dash'); renderizarGeral();
        }

        function montarMenu() {
            const m = document.getElementById('sidebar-menu');
            let h = `<div class="menu-item active" onclick="showTab('tab-dash')">Dashboard</div>`;
            if(sessao.role !== 'aluno') {
                h += `<div class="menu-item" onclick="showTab('tab-matricula')">Matrículas</div>`;
                h += `<div class="menu-item" onclick="showTab('tab-frequencia')">Frequência</div>`;
                h += `<div class="menu-item" onclick="showTab('tab-lab')">Laboratório</div>`;
                h += `<div class="menu-item" onclick="showTab('tab-formados')">Formados</div>`;
            }
            if(sessao.role === 'admin') h += `<div class="menu-item" onclick="showTab('tab-config')">Configurações</div>`;
            if(sessao.role === 'aluno') h += `<div class="menu-item" onclick="showTab('tab-aluno')">Meu Boletim</div>`;
            m.innerHTML = h;
        }

        function cadastrarAluno() {
            const nome = document.getElementById('m-nome').value, curso = document.getElementById('m-curso').value,
                  user = document.getElementById('m-user').value, pass = document.getElementById('m-pass').value,
                  tel = document.getElementById('m-tel').value, resp = document.getElementById('m-resp').value,
                  endereco = document.getElementById('m-end').value;
            if(!nome || !user) return;
            db.alunos.push({ id: Date.now(), nome, curso, user, pass, tel, resp, endereco, freq: Array(12).fill().map(() => Array(4).fill('P')) });
            salvar(); renderizarGeral();
            // Limpar campos
            ['m-nome','m-curso','m-user','m-tel','m-resp','m-end'].forEach(id => document.getElementById(id).value = "");
        }

        function renderizarGeral() {
            document.getElementById('st-alunos').innerText = db.alunos.length;
            document.getElementById('st-pcs').innerText = db.pcs.filter(p=>p.status==='free').length + '/8';
            document.getElementById('st-form').innerText = db.formados.length;
            document.getElementById('mural-view').innerText = db.mural;

            document.getElementById('vitrine-area').innerHTML = db.vitrine.map(c => `<div style="background:var(--primary); color:#000; padding:5px 12px; border-radius:20px; font-size:0.8rem; font-weight:bold">${c}</div>`).join('');
            document.getElementById('vitrine-edit-list').innerHTML = db.vitrine.map((c, i) => `<div style="display:flex; justify-content:space-between; padding:8px; border-bottom:1px solid #1e293b"><span>${c}</span><button class="btn-danger" onclick="delCurso(${i})">X</button></div>`).join('');

            document.getElementById('list-alunos').innerHTML = db.alunos.map(a => `
                <tr>
                    <td>${a.nome}</td><td>${a.curso}</td><td>${a.endereco || '---'}</td><td>${a.tel}</td><td>${a.resp}</td>
                    <td class="no-print"><small>${a.user} / ${a.pass}</small></td>
                    <td class="no-print">
                        <button class="btn-primary" onclick="formarAluno(${a.id})">Formar</button>
                        <button class="btn-danger" onclick="excluirAluno(${a.id})">X</button>
                    </td>
                </tr>
            `).join('');

            document.getElementById('list-func').innerHTML = db.funcionarios.map(f => `<tr><td>${f.user}</td><td>${f.pass}</td><td>${f.role}</td><td><button class="btn-danger" onclick="delFunc('${f.user}')">X</button></td></tr>`).join('');
            document.getElementById('list-formados').innerHTML = db.formados.map(a => `<tr><td>${a.nome}</td><td>${a.curso}</td><td class="no-print"><button class="btn-primary" onclick="reativar(${a.id})">Reativar</button> <button class="btn-danger" onclick="excluirFormado(${a.id})">X</button></td></tr>`).join('');
            
            renderPCs();
        }

        function renderPCs() { 
            document.getElementById('pc-grid-view').innerHTML = db.pcs.map(p => `
                <div class="pc-item ${p.status}" onclick="abrirPC(${p.id})">
                    <b>PC 0${p.id}</b><br>
                    <small>${p.status === 'free' ? 'LIVRE' : p.status === 'busy' ? 'RESERVADO' : 'MANUTENÇÃO'}</small>
                </div>
            `).join(''); 
        }

        function abrirPC(id) { 
            if(sessao.role === 'aluno') return; 
            pcAtivoId = id; 
            const pc = db.pcs.find(x => x.id === id); 
            document.getElementById('pc-edit-card').classList.remove('hidden'); 
            document.getElementById('pc-info-text').value = pc.info; 
            document.getElementById('pc-status-sel').value = pc.status; 
            document.getElementById('pc-title-edit').innerText = "Configurar PC 0" + id;
        }

        function salvarPC() { 
            const pc = db.pcs.find(x => x.id === pcAtivoId); 
            pc.info = document.getElementById('pc-info-text').value; 
            pc.status = document.getElementById('pc-status-sel').value; 
            salvar(); renderizarGeral(); 
            document.getElementById('pc-edit-card').classList.add('hidden'); 
        }

        function addFuncionario() { const u = document.getElementById('f-user').value, p = document.getElementById('f-pass').value, r = document.getElementById('f-role').value; if(u && p) { db.funcionarios.push({user: u, pass: p, role: r}); salvar(); renderizarGeral(); } }
        function addCourseVitrine() { const c = document.getElementById('new-course').value; if(c) { db.vitrine.push(c); salvar(); renderizarGeral(); } }
        function delCurso(i) { db.vitrine.splice(i, 1); salvar(); renderizarGeral(); }
        function delFunc(u) { db.funcionarios = db.funcionarios.filter(x=>x.user!==u); salvar(); renderizarGeral(); }
        function excluirAluno(id) { db.alunos = db.alunos.filter(x=>x.id!==id); salvar(); renderizarGeral(); }
        function excluirFormado(id) { db.formados = db.formados.filter(x=>x.id!==id); salvar(); renderizarGeral(); }
        function formarAluno(id) { const idx = db.alunos.findIndex(x => x.id === id); const a = db.alunos.splice(idx, 1)[0]; db.formados.push(a); salvar(); renderizarGeral(); }
        function reativar(id) { const idx = db.formados.findIndex(x => x.id === id); const a = db.formados.splice(idx, 1)[0]; db.alunos.push(a); salvar(); renderizarGeral(); }
        
        function showTab(id) {
            document.querySelectorAll('.tab-view').forEach(v => v.classList.add('hidden'));
            document.querySelectorAll('.menu-item').forEach(m => m.classList.remove('active'));
            document.getElementById(id).classList.remove('hidden');
            if(id === 'tab-frequencia') renderFreq();
            if(id === 'tab-aluno') renderPortalAluno();
        }

        function renderFreq() {
            document.getElementById('freq-area').innerHTML = db.alunos.map(a => `<div class="card glass"><b>${a.nome}</b><div class="freq-row">${a.freq.map((m, im) => `<div class="month-box"><small>${MESES[im]}</small><br>${m.map((s, is) => `<div class="wk-btn ${s.toLowerCase()}-bg" onclick="altF(${a.id},${im},${is})">${s}</div>`).join('')}</div>`).join('')}</div></div>`).join('');
        }

        function altF(aid, im, is) { const a = db.alunos.find(x => x.id === aid); const c = {'P':'F', 'F':'FJ', 'FJ':'P'}; a.freq[im][is] = c[a.freq[im][is]]; salvar(); renderFreq(); }

        function renderPortalAluno() {
            const a = db.alunos.find(x => x.user === sessao.user); if(!a) return;
            document.getElementById('al-nome-display').innerText = a.nome;
            document.getElementById('al-curso-display').innerText = "CURSO: " + a.curso;
            document.getElementById('al-freq-display').innerHTML = `<div class="freq-row">${a.freq.map((m, im) => `<div class="month-box"><small>${MESES[im]}</small><br>${m.map(s => `<div class="wk-btn ${s.toLowerCase()}-bg">${s}</div>`).join('')}</div>`).join('')}</div>`;
        }

        function salvar() { localStorage.setItem('labinfo_v6_pdf', JSON.stringify(db)); }
    </script>
</body>
</html>
