<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reporte RSU - 20 Escuelas UAC</title>
    
    <!-- Optimización para buscadores y redes sociales -->
    <meta name="description" content="Reporte de Gestión RSU 2025-II - Universidad Andina del Cusco">
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');
        
        :root {
            --azul-uac-oscuro: #1F3F6E;
            --azul-uac-medio: #2C5D9F;
            --azul-uac-claro: #27A9C9;
            --blanco: #FFFFFF;
            --gris-oscuro: #333333;
            --gris-claro: #E9E9E9;
            --azul-navy: #162F52;
            --gris-medio: #6F7C8A;
        }

        body { 
            font-family: 'Inter', sans-serif; 
            background-color: var(--gris-claro); 
            color: var(--gris-oscuro);
            margin: 0;
            padding: 0;
        }

        /* Contenedor de imagen optimizado */
        .hero-banner {
            width: 100%;
            background-color: var(--blanco);
            display: flex;
            justify-content: center;
            align-items: center;
            border-bottom: 4px solid var(--azul-uac-claro);
        }

        .hero-banner img {
            max-width: 100%;
            height: auto;
            max-height: 150px; /* Tamaño regulado para que no domine toda la pantalla */
            object-fit: contain;
            padding: 1rem;
        }

        .header-uac {
            background-color: var(--azul-uac-oscuro);
            color: var(--blanco);
        }

        .card-uac {
            background-color: var(--blanco);
            border: 1px solid #e5e7eb;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .card-uac:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 24px -10px rgba(0, 0, 0, 0.2);
            border-color: var(--azul-uac-claro);
        }

        .status-dot {
            height: 8px;
            width: 8px;
            border-radius: 50%;
            display: inline-block;
        }

        /* Scrollbar personalizado para GitHub Pages */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: var(--gris-claro);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--azul-uac-medio);
            border-radius: 4px;
        }
    </style>
</head>
<body class="antialiased">

    <!-- Banner de Imagen Regulado -->
    <header class="max-w-7xl mx-auto mt-0 md:mt-4 overflow-hidden md:rounded-t-xl shadow-sm">
        <div class="hero-banner">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGkTWwWeUANXVDNgrEEpvdV_iTAuuTHar2eA&s" 
                 alt="Logo Universidad Andina del Cusco">
        </div>
        
        <!-- Información Institucional -->
        <div class="p-6 header-uac">
            <div class="flex flex-col lg:flex-row justify-between items-center gap-6">
                <div class="flex items-center gap-4">
                    <div class="hidden sm:block bg-white/10 p-3 rounded-full">
                        <i class="fas fa-university text-2xl text-white"></i>
                    </div>
                    <div class="text-center lg:text-left">
                        <h1 class="text-xl md:text-2xl font-bold tracking-tight uppercase">Gestión RSU 2025-II</h1>
                        <p class="text-xs md:text-sm font-light opacity-80">Dirección de Responsabilidad Social Universitaria</p>
                    </div>
                </div>
                
                <div class="flex items-center gap-3">
                    <div class="bg-white/10 px-4 py-2 rounded-lg border border-white/20 text-center min-w-[100px]">
                        <span class="block text-2xl font-bold">20</span>
                        <span class="text-[9px] uppercase font-bold text-white/70">Escuelas</span>
                    </div>
                    <div class="bg-white px-4 py-2 rounded-lg text-center min-w-[100px] shadow-sm">
                        <span class="block text-2xl font-bold" style="color: var(--azul-uac-oscuro);">100%</span>
                        <span class="text-[9px] uppercase font-bold" style="color: var(--azul-uac-medio);">Aprobado</span>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Contenido Principal -->
    <main class="max-w-7xl mx-auto px-4 py-8">
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-5" id="schoolsGrid">
            <!-- Las tarjetas se generan vía JavaScript -->
        </div>
    </main>

    <!-- Footer -->
    <footer class="max-w-7xl mx-auto px-6 py-10 text-center border-t border-gray-300">
        <p class="text-xs font-semibold tracking-widest uppercase mb-4" style="color: var(--gris-medio);">
            © 2025 Universidad Andina del Cusco
        </p>
        <div class="flex justify-center gap-3">
            <div class="w-8 h-1 rounded-full" style="background-color: var(--azul-uac-oscuro);"></div>
            <div class="w-8 h-1 rounded-full" style="background-color: var(--azul-uac-medio);"></div>
            <div class="w-8 h-1 rounded-full" style="background-color: var(--azul-uac-claro);"></div>
        </div>
    </footer>

    <script>
        const schools = [
            { name: "Derecho", faculty: "Derecho y Cs. Políticas", icon: "fa-balance-scale", programs: 2, projects: 4, detail: "Derecho Ambiental, DD.HH. y Tributario." },
            { name: "Ing. de Sistemas", faculty: "Ingeniería y Arquitectura", icon: "fa-laptop-code", programs: 4, projects: 2, detail: "Habilidades digitales e incubación tecnológica." },
            { name: "Ing. Industrial", faculty: "Ingeniería y Arquitectura", icon: "fa-industry", programs: 1, projects: 6, detail: "Seguridad industrial y gestión productiva." },
            { name: "Ing. Civil", faculty: "Ingeniería y Arquitectura", icon: "fa-hard-hat", programs: 3, projects: 4, detail: "Infraestructura segura y evaluación de viviendas." },
            { name: "Ing. Ambiental", faculty: "Ingeniería y Arquitectura", icon: "fa-leaf", programs: 4, projects: 4, detail: "Gestión de recursos y remediación ambiental." },
            { name: "Arquitectura", faculty: "Ingeniería y Arquitectura", icon: "fa-drafting-compass", programs: 1, projects: 4, detail: "Diseño participativo y urbanismo social." },
            { name: "Medicina Humana", faculty: "Ciencias de la Salud", icon: "fa-user-md", programs: 2, projects: 2, detail: "Cultura Ambiental y Anemia en Instituciones." },
            { name: "Estomatología", faculty: "Ciencias de la Salud", icon: "fa-tooth", programs: 2, projects: 4, detail: "Salud Oral y Brigada Verde (Machupicchu)." },
            { name: "Psicología", faculty: "Ciencias de la Salud", icon: "fa-brain", programs: 2, projects: 3, detail: "Salud mental y conducta infantil comunitaria." },
            { name: "Obstetricia", faculty: "Ciencias de la Salud", icon: "fa-baby-carriage", programs: 2, projects: 2, detail: "Salud Sexual Reproductiva y Residuos Sólidos." },
            { name: "Enfermería", faculty: "Ciencias de la Salud", icon: "fa-user-nurse", programs: 0, projects: 3, detail: "Cuidados comunitarios e intervención primaria." },
            { name: "Tecnología Médica", faculty: "Ciencias de la Salud", icon: "fa-microscope", programs: 1, projects: 3, detail: "Prevención músculo esquelética y adulto mayor." },
            { name: "Marketing", faculty: "Ciencias Económicas", icon: "fa-bullhorn", programs: 2, projects: 7, detail: "Expobranding y Marketing Digital Social." },
            { name: "Negocios Int.", faculty: "Ciencias Económicas", icon: "fa-globe-americas", programs: 4, projects: 0, detail: "Gestión de comercio exterior y exportación." },
            { name: "Contabilidad", faculty: "Ciencias Económicas", icon: "fa-calculator", programs: 5, projects: 3, detail: "Cultura tributaria y finanzas públicas." },
            { name: "Economía", faculty: "Ciencias Económicas", icon: "fa-chart-pie", programs: 3, projects: 3, detail: "Proyectos productivos y educación financiera." },
            { name: "Administración", faculty: "Ciencias Económicas", icon: "fa-briefcase", programs: 2, projects: 2, detail: "Gestión empresarial e incubación de negocios." },
            { name: "Finanzas", faculty: "Ciencias Económicas", icon: "fa-coins", programs: 4, projects: 4, detail: "Inclusión financiera y mercados de capitales." },
            { name: "Turismo", faculty: "Ciencias Económicas", icon: "fa-plane", programs: 0, projects: 0, detail: "Sin registros vigentes en este periodo." },
            { name: "Educación", faculty: "Ciencias y Humanidades", icon: "fa-chalkboard-teacher", programs: 0, projects: 5, detail: "Pedagogía ambiental y refuerzo educativo." }
        ];

        const grid = document.getElementById('schoolsGrid');

        schools.forEach(school => {
            const hasActivity = (school.programs + school.projects) > 0;
            const statusColor = hasActivity ? 'var(--azul-uac-claro)' : '#9ca3af';

            const card = document.createElement('div');
            card.className = 'card-uac rounded-xl p-5 flex flex-col h-full';
            card.innerHTML = `
                <div class="flex items-center gap-4 mb-5">
                    <div class="w-12 h-12 flex items-center justify-center rounded-lg shadow-sm shrink-0" 
                         style="background-color: var(--azul-uac-oscuro); color: white;">
                        <i class="fas ${school.icon} text-lg"></i>
                    </div>
                    <div class="overflow-hidden">
                        <h3 class="font-bold text-slate-800 text-sm md:text-base truncate">${school.name}</h3>
                        <p class="text-[9px] font-bold uppercase tracking-wider text-slate-400 truncate">${school.faculty}</p>
                    </div>
                </div>
                
                <div class="flex-grow space-y-4">
                    <div class="grid grid-cols-2 gap-2">
                        <div class="bg-gray-50 p-2 rounded-lg border border-gray-100 text-center">
                            <span class="block text-xl font-bold" style="color: var(--azul-uac-oscuro);">${school.programs}</span>
                            <span class="text-[8px] uppercase font-bold text-slate-400">Programas</span>
                        </div>
                        <div class="bg-gray-50 p-2 rounded-lg border border-gray-100 text-center">
                            <span class="block text-xl font-bold" style="color: var(--azul-uac-medio);">${school.projects}</span>
                            <span class="text-[8px] uppercase font-bold text-slate-400">Proyectos</span>
                        </div>
                    </div>
                    
                    <div class="pt-3 border-t border-gray-100">
                        <span class="text-[9px] font-black uppercase text-slate-300 block mb-1">Impacto Directo</span>
                        <p class="text-xs text-slate-600 leading-snug line-clamp-2">${school.detail}</p>
                    </div>
                </div>
                
                <div class="mt-5 pt-4 border-t border-gray-50 flex items-center justify-between">
                    <div class="flex items-center gap-2">
                        <span class="status-dot ${hasActivity ? 'animate-pulse' : ''}" style="background-color: ${statusColor}"></span>
                        <span class="text-[9px] font-bold uppercase" style="color: ${statusColor}">
                            ${hasActivity ? 'En Ejecución' : 'Pendiente'}
                        </span>
                    </div>
                    <button class="text-[9px] font-bold px-3 py-1.5 rounded border border-gray-200 hover:bg-gray-50 transition-colors"
                            style="color: var(--azul-uac-medio);">
                        DETALLES
                    </button>
                </div>
            `;
            grid.appendChild(card);
        });
    </script>
</body>
</html>
