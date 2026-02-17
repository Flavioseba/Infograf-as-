<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reporte RSU - 20 Escuelas UAC</title>
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
        }

        .header-uac {
            background-color: var(--azul-uac-oscuro);
            color: var(--blanco);
        }

        .card-uac {
            background-color: var(--blanco);
            border: 1px solid #d1d5db;
            transition: all 0.3s ease;
        }

        .card-uac:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            border-color: var(--azul-uac-medio);
        }

        .hero-image-container {
            width: 100%;
            height: 180px; /* Altura regulada */
            background-color: var(--azul-uac-oscuro); /* Fondo para que no queden huecos blancos si la imagen es ancha */
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .hero-image {
            width: 100%;
            height: 100%;
            object-fit: contain; /* Asegura que se vea toda la imagen sin recortes */
            padding: 10px; /* Espaciado interno para que no toque los bordes */
        }
    </style>
</head>
<body class="p-0 md:p-6">

    <!-- Header Principal -->
    <div class="max-w-7xl mx-auto mb-8 bg-white rounded-xl shadow-lg overflow-hidden border border-gray-200">
        <!-- Contenedor regulado de imagen -->
        <div class="hero-image-container">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGkTWwWeUANXVDNgrEEpvdV_iTAuuTHar2eA&s" 
                 alt="Encabezado UAC" 
                 class="hero-image">
        </div>
        
        <div class="p-6 flex flex-col md:flex-row justify-between items-center header-uac">
            <div class="flex items-center gap-5">
                <div class="bg-white p-3 rounded-lg shadow-inner">
                    <i class="fas fa-university text-3xl" style="color: var(--azul-uac-oscuro);"></i>
                </div>
                <div>
                    <h1 class="text-2xl md:text-3xl font-bold tracking-tight">Reporte de Gestión RSU 2025-II</h1>
                    <p class="opacity-90 font-light">Dirección de Responsabilidad Social Universitaria • Universidad Andina del Cusco</p>
                </div>
            </div>
            <div class="flex gap-4 mt-6 md:mt-0">
                <div class="text-center px-6 py-3 bg-white/10 backdrop-blur-md rounded-lg border border-white/20">
                    <span class="block text-3xl font-bold text-white">20</span>
                    <span class="text-[10px] font-bold uppercase tracking-widest text-white/80">Escuelas</span>
                </div>
                <div class="text-center px-6 py-3 bg-white rounded-lg shadow-md">
                    <span class="block text-3xl font-bold" style="color: var(--azul-uac-oscuro);">100%</span>
                    <span class="text-[10px] font-bold uppercase tracking-widest" style="color: var(--azul-uac-medio);">Aprobado</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Grid de Escuelas -->
    <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6 px-4 md:px-0" id="schoolsGrid">
        <!-- Generación dinámica -->
    </div>

    <!-- Footer -->
    <div class="max-w-7xl mx-auto mt-12 mb-8 p-6 text-center border-t border-gray-300">
        <p class="text-sm font-medium" style="color: var(--gris-medio);">
            © 2025 Universidad Andina del Cusco - Dirección de Responsabilidad Social y Extensión Universitaria
        </p>
        <div class="flex justify-center gap-4 mt-2">
            <span class="w-3 h-3 rounded-full" style="background-color: var(--azul-uac-oscuro);"></span>
            <span class="w-3 h-3 rounded-full" style="background-color: var(--azul-uac-medio);"></span>
            <span class="w-3 h-3 rounded-full" style="background-color: var(--azul-uac-claro);"></span>
        </div>
    </div>

    <script>
        const schools = [
            { name: "Derecho", faculty: "Derecho y Cs. Políticas", icon: "fa-balance-scale", color: "azul-navy", programs: 2, projects: 4, detail: "Derecho Ambiental, DD.HH. y Tributario." },
            { name: "Ingeniería de Sistemas", faculty: "Ingeniería y Arquitectura", icon: "fa-laptop-code", color: "azul-navy", programs: 4, projects: 2, detail: "Habilidades digitales e incubación tecnológica." },
            { name: "Ingeniería Industrial", faculty: "Ingeniería y Arquitectura", icon: "fa-industry", color: "azul-navy", programs: 1, projects: 6, detail: "Seguridad industrial y emprendimientos productivos." },
            { name: "Ingeniería Civil", faculty: "Ingeniería y Arquitectura", icon: "fa-hard-hat", color: "azul-navy", programs: 3, projects: 4, detail: "Infraestructura segura y evaluación de viviendas." },
            { name: "Ingeniería Ambiental", faculty: "Ingeniería y Arquitectura", icon: "fa-leaf", color: "azul-navy", programs: 4, projects: 4, detail: "Gestión de recursos y remediación ambiental." },
            { name: "Arquitectura", faculty: "Ingeniería y Arquitectura", icon: "fa-drafting-compass", color: "azul-navy", programs: 1, projects: 4, detail: "Diseño participativo y urbanismo social." },
            { name: "Medicina Humana", faculty: "Ciencias de la Salud", icon: "fa-user-md", color: "azul-navy", programs: 2, projects: 2, detail: "Cultura Ambiental y Anemia en I.E." },
            { name: "Estomatología", faculty: "Ciencias de la Salud", icon: "fa-tooth", color: "azul-navy", programs: 2, projects: 4, detail: "Salud Oral y Brigada Verde (Machupicchu)." },
            { name: "Psicología", faculty: "Ciencias de la Salud", icon: "fa-brain", color: "azul-navy", programs: 2, projects: 3, detail: "Acoso sexual, conducta infantil y salud mental." },
            { name: "Obstetricia", faculty: "Ciencias de la Salud", icon: "fa-baby-carriage", color: "azul-navy", programs: 2, projects: 2, detail: "Salud Sexual Reproductiva y Residuos Sólidos." },
            { name: "Enfermería", faculty: "Ciencias de la Salud", icon: "fa-user-nurse", color: "azul-navy", programs: 0, projects: 3, detail: "Cuidados comunitarios e intervención primaria." },
            { name: "Tecnología Médica", faculty: "Ciencias de la Salud", icon: "fa-microscope", color: "azul-navy", programs: 1, projects: 3, detail: "Prevención músculo esquelética y adulto mayor." },
            { name: "Marketing", faculty: "Ciencias Económicas", icon: "fa-bullhorn", color: "azul-navy", programs: 2, projects: 7, detail: "Expobranding y Marketing Digital/Visual." },
            { name: "Negocios Internacionales", faculty: "Ciencias Económicas", icon: "fa-globe-americas", color: "azul-navy", programs: 4, projects: 0, detail: "Gestión de comercio exterior y exportación." },
            { name: "Contabilidad", faculty: "Ciencias Económicas", icon: "fa-calculator", color: "azul-navy", programs: 5, projects: 3, detail: "Cultura tributaria y finanzas públicas." },
            { name: "Economía", faculty: "Ciencias Económicas", icon: "fa-chart-pie", color: "azul-navy", programs: 3, projects: 3, detail: "Proyectos productivos y educación financiera." },
            { name: "Administración", faculty: "Ciencias Económicas", icon: "fa-briefcase", color: "azul-navy", programs: 2, projects: 2, detail: "Gestión empresarial e incubación de negocios." },
            { name: "Finanzas", faculty: "Ciencias Económicas", icon: "fa-coins", color: "azul-navy", programs: 4, projects: 4, detail: "Inclusión financiera y mercados de capitales." },
            { name: "Turismo", faculty: "Ciencias Económicas", icon: "fa-plane", color: "azul-navy", programs: 0, projects: 0, detail: "Sin registros vigentes en este periodo." },
            { name: "Educación", faculty: "Ciencias y Humanidades", icon: "fa-chalkboard-teacher", color: "azul-navy", programs: 0, projects: 5, detail: "Pedagogía ambiental y refuerzo educativo." }
        ];

        const grid = document.getElementById('schoolsGrid');

        schools.forEach(school => {
            const card = document.createElement('div');
            card.className = `card-uac rounded-xl p-6 flex flex-col h-full`;
            
            const total = school.programs + school.projects;
            const statusColor = total > 0 ? 'var(--azul-uac-claro)' : '#cbd5e1';

            card.innerHTML = `
                <div class="flex justify-between items-start mb-4">
                    <div class="flex items-center gap-4">
                        <div class="p-3 rounded-lg shadow-sm" style="background-color: var(--azul-uac-oscuro); color: white;">
                            <i class="fas ${school.icon} text-xl"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-slate-800 text-base leading-tight">${school.name}</h3>
                            <p class="text-[10px] text-slate-500 mt-1 uppercase font-bold tracking-wider">${school.faculty}</p>
                        </div>
                    </div>
                </div>
                
                <div class="flex-grow">
                    <div class="grid grid-cols-2 gap-3 mb-4">
                        <div class="bg-gray-50 p-3 rounded-lg border border-gray-100 text-center">
                            <span class="block text-2xl font-bold" style="color: var(--azul-uac-oscuro);">${school.programs}</span>
                            <span class="text-[9px] uppercase font-bold text-slate-400">Programas</span>
                        </div>
                        <div class="bg-gray-50 p-3 rounded-lg border border-gray-100 text-center">
                            <span class="block text-2xl font-bold" style="color: var(--azul-uac-medio);">${school.projects}</span>
                            <span class="text-[9px] uppercase font-bold text-slate-400">Proyectos</span>
                        </div>
                    </div>
                    
                    <div class="space-y-3">
                        <div class="pt-3 border-t border-gray-100">
                            <p class="text-[10px] uppercase font-black text-slate-400 mb-1 tracking-tighter">Impacto RSU</p>
                            <p class="text-xs text-slate-600 italic leading-relaxed line-clamp-3">${school.detail}</p>
                        </div>
                    </div>
                </div>
                
                <div class="mt-6 pt-4 border-t border-gray-50 flex items-center justify-between">
                    <span class="text-[10px] font-black uppercase flex items-center gap-2" style="color: ${statusColor}">
                        <span class="relative flex h-2 w-2">
                            ${total > 0 ? `<span class="animate-ping absolute inline-flex h-full w-full rounded-full opacity-75" style="background-color: ${statusColor}"></span>` : ''}
                            <span class="relative inline-flex rounded-full h-2 w-2" style="background-color: ${statusColor}"></span>
                        </span>
                        ${total > 0 ? 'En Ejecución' : 'En Espera'}
                    </span>
                    <button class="text-[10px] font-bold py-1 px-3 rounded-md transition-colors hover:bg-gray-100" style="color: var(--azul-uac-medio); border: 1px solid var(--azul-uac-medio);">
                        VER PLAN
                    </button>
                </div>
            `;
            grid.appendChild(card);
        });
    </script>
</body>
</html>
