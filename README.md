<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reporte RSU - 20 Escuelas</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');
        body { font-family: 'Inter', sans-serif; background-color: #f3f4f6; }
        .card-hover:hover { transform: translateY(-2px); box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); }
    </style>
</head>
<body class="p-4 bg-gray-100 text-slate-800">

    <!-- Header -->
    <div class="max-w-7xl mx-auto mb-8 flex flex-col md:flex-row justify-between items-center bg-white p-6 rounded-xl shadow-sm border border-gray-200">
        <div class="flex items-center gap-4">
            <div class="bg-blue-600 text-white p-4 rounded-lg">
                <i class="fas fa-university text-3xl"></i>
            </div>
            <div>
                <h1 class="text-2xl font-bold text-slate-900">Reporte de Gestión RSU 2025-II</h1>
                <p class="text-slate-500">Cobertura: 20 Escuelas Profesionales • Universidad Andina del Cusco</p>
            </div>
        </div>
        <div class="flex gap-4 mt-4 md:mt-0">
            <div class="text-center px-4 py-2 bg-green-50 rounded-lg border border-green-100">
                <span class="block text-2xl font-bold text-green-600">100%</span>
                <span class="text-xs font-bold text-green-700 uppercase">Planes Aprobados</span>
            </div>
            <div class="text-center px-4 py-2 bg-blue-50 rounded-lg border border-blue-100">
                <span class="block text-2xl font-bold text-blue-600">20</span>
                <span class="text-xs font-bold text-blue-700 uppercase">Escuelas Activas</span>
            </div>
        </div>
    </div>

    <!-- Grid de Escuelas -->
    <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4" id="schoolsGrid">
        <!-- Generación dinámica -->
    </div>

    <!-- Footer -->
    <div class="max-w-7xl mx-auto mt-8 text-center text-slate-400 text-sm">
        <p>Datos actualizados según revisión detallada de programas y proyectos por escuela profesional.</p>
    </div>

    <script>
        const schools = [
            // --- DERECHO ---
            { name: "Derecho", faculty: "Derecho y Cs. Políticas", icon: "fa-balance-scale", color: "red", programs: 2, projects: 4, detail: "Derecho Ambiental, DD.HH. y Tributario." },
            
            // --- INGENIERÍA Y ARQUITECTURA ---
            { name: "Ingeniería de Sistemas", faculty: "Ingeniería y Arquitectura", icon: "fa-laptop-code", color: "blue", programs: 4, projects: 2, detail: "Habilidades digitales e incubación tecnológica." },
            { name: "Ingeniería Industrial", faculty: "Ingeniería y Arquitectura", icon: "fa-industry", color: "blue", programs: 1, projects: 6, detail: "Seguridad industrial y emprendimientos productivos." },
            { name: "Ingeniería Civil", faculty: "Ingeniería y Arquitectura", icon: "fa-hard-hat", color: "blue", programs: 3, projects: 4, detail: "Infraestructura segura y evaluación de viviendas." },
            { name: "Ingeniería Ambiental", faculty: "Ingeniería y Arquitectura", icon: "fa-leaf", color: "blue", programs: 4, projects: 4, detail: "Gestión de recursos y remediación ambiental." },
            { name: "Arquitectura", faculty: "Ingeniería y Arquitectura", icon: "fa-drafting-compass", color: "blue", programs: 1, projects: 4, detail: "Diseño participativo y urbanismo social." },

            // --- SALUD ---
            { name: "Medicina Humana", faculty: "Ciencias de la Salud", icon: "fa-user-md", color: "emerald", programs: 2, projects: 2, detail: "Cultura Ambiental y Anemia en I.E." },
            { name: "Estomatología", faculty: "Ciencias de la Salud", icon: "fa-tooth", color: "emerald", programs: 2, projects: 4, detail: "Salud Oral y Brigada Verde (Machupicchu)." },
            { name: "Psicología", faculty: "Ciencias de la Salud", icon: "fa-brain", color: "emerald", programs: 2, projects: 3, detail: "Acoso sexual, conducta infantil y salud mental." },
            { name: "Obstetricia", faculty: "Ciencias de la Salud", icon: "fa-baby-carriage", color: "emerald", programs: 2, projects: 2, detail: "Salud Sexual Reproductiva y Residuos Sólidos." },
            { name: "Enfermería", faculty: "Ciencias de la Salud", icon: "fa-user-nurse", color: "emerald", programs: 0, projects: 3, detail: "Cuidados comunitarios e intervención primaria." },
            { name: "Tecnología Médica", faculty: "Ciencias de la Salud", icon: "fa-microscope", color: "emerald", programs: 1, projects: 3, detail: "Prevención músculo esquelética y adulto mayor." },

            // --- ECONÓMICAS ---
            { name: "Marketing", faculty: "Ciencias Económicas", icon: "fa-bullhorn", color: "amber", programs: 2, projects: 7, detail: "Expobranding y Marketing Digital/Visual." },
            { name: "Negocios Internacionales", faculty: "Ciencias Económicas", icon: "fa-globe-americas", color: "amber", programs: 4, projects: 0, detail: "Gestión de comercio exterior y exportación." },
            { name: "Contabilidad", faculty: "Ciencias Económicas", icon: "fa-calculator", color: "amber", programs: 5, projects: 3, detail: "Cultura tributaria y finanzas públicas." },
            { name: "Economía", faculty: "Ciencias Económicas", icon: "fa-chart-pie", color: "amber", programs: 3, projects: 3, detail: "Proyectos productivos y educación financiera." },
            { name: "Administración", faculty: "Ciencias Económicas", icon: "fa-briefcase", color: "amber", programs: 2, projects: 2, detail: "Gestión empresarial e incubación de negocios." },
            { name: "Finanzas", faculty: "Ciencias Económicas", icon: "fa-coins", color: "amber", programs: 4, projects: 4, detail: "Inclusión financiera y mercados de capitales." },
            { name: "Turismo", faculty: "Ciencias Económicas", icon: "fa-plane", color: "amber", programs: 0, projects: 0, detail: "Sin registros vigentes en este periodo." },

            // --- HUMANIDADES ---
            { name: "Educación", faculty: "Ciencias y Humanidades", icon: "fa-chalkboard-teacher", color: "violet", programs: 0, projects: 5, detail: "Pedagogía ambiental y refuerzo educativo." }
        ];

        const grid = document.getElementById('schoolsGrid');
        const colorClasses = {
            red: 'bg-red-50 text-red-600 border-red-200',
            blue: 'bg-blue-50 text-blue-600 border-blue-200',
            emerald: 'bg-emerald-50 text-emerald-600 border-emerald-200',
            amber: 'bg-amber-50 text-amber-600 border-amber-200',
            violet: 'bg-violet-50 text-violet-600 border-violet-200'
        };
        const iconBgClasses = {
            red: 'bg-red-100', blue: 'bg-blue-100', emerald: 'bg-emerald-100', amber: 'bg-amber-100', violet: 'bg-violet-100'
        };

        schools.forEach(school => {
            const card = document.createElement('div');
            card.className = `bg-white rounded-xl p-5 border border-slate-200 card-hover transition-all duration-300 flex flex-col h-full`;
            card.innerHTML = `
                <div class="flex justify-between items-start mb-3">
                    <div class="flex items-center gap-3">
                        <div class="p-2 rounded-lg ${iconBgClasses[school.color]} ${colorClasses[school.color].split(' ')[1]}">
                            <i class="fas ${school.icon} text-lg"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-slate-800 text-sm leading-tight">${school.name}</h3>
                            <p class="text-[10px] text-slate-400 mt-0.5 uppercase font-semibold">${school.faculty}</p>
                        </div>
                    </div>
                </div>
                
                <div class="flex-grow">
                    <div class="grid grid-cols-2 gap-2 mb-3">
                        <div class="bg-slate-50 p-2 rounded border border-slate-100 text-center">
                            <span class="block text-lg font-bold text-blue-700">${school.programs}</span>
                            <span class="text-[9px] uppercase font-bold text-slate-400">Programas</span>
                        </div>
                        <div class="bg-slate-50 p-2 rounded border border-slate-100 text-center">
                            <span class="block text-lg font-bold text-amber-700">${school.projects}</span>
                            <span class="text-[9px] uppercase font-bold text-slate-400">Proyectos</span>
                        </div>
                    </div>
                    
                    <div class="space-y-2">
                        <div class="pt-2 border-t border-slate-100">
                            <p class="text-[10px] uppercase font-bold text-slate-400 mb-0.5">Enfoque RSU</p>
                            <p class="text-xs text-slate-600 italic line-clamp-2 leading-tight">${school.detail}</p>
                        </div>
                    </div>
                </div>
                
                <div class="mt-4 pt-3 border-t border-slate-50 flex items-center justify-between">
                    <span class="${school.programs + school.projects > 0 ? 'text-green-500' : 'text-slate-300'} text-[10px] font-bold">
                        <i class="fas fa-circle text-[8px] mr-1"></i> ${school.programs + school.projects > 0 ? 'ACTIVO' : 'SIN REGISTRO'}
                    </span>
                    <i class="fas fa-chevron-right text-slate-200 text-xs"></i>
                </div>
            `;
            grid.appendChild(card);
        });
    </script>
</body>
</html>
