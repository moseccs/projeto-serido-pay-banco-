<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SeridoPay - Seu Banco Digital</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }
        
        .primary-bg {
            background: linear-gradient(135deg, #FF7B25 0%, #4CAF50 100%);
        }
        
        .primary-text {
            background: linear-gradient(135deg, #FF7B25 0%, #4CAF50 100%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .dropdown:hover .dropdown-menu {
            display: block;
        }
        
        .mobile-menu {
            transition: all 0.3s ease;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header/Navbar -->
    <header class="sticky top-0 z-50 bg-white shadow-sm">
        <div class="container mx-auto px-4 py-3">
            <div class="flex justify-between items-center">
                <!-- Logo -->
                <div class="flex items-center">
                    <a href="#" class="text-2xl font-bold">
                        <span class="primary-text">SERIDO</span><span class="text-gray-800">PAY</span>
                    </a>
                </div>
                
                <!-- Desktop Navigation -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#" class="text-gray-700 hover:text-orange-500 font-medium">Início</a>
                    <a href="#" class="text-gray-700 hover:text-orange-500 font-medium">Conta</a>
                    <a href="#" class="text-gray-700 hover:text-orange-500 font-medium">Cartões</a>
                    <a href="#" class="text-gray-700 hover:text-orange-500 font-medium">Investimentos</a>
                    <a href="#" class="text-gray-700 hover:text-orange-500 font-medium">Ajuda</a>
                </nav>
                
                <!-- User Area -->
                <div class="flex items-center space-x-5">
                    <div class="dropdown relative">
                        <button class="flex items-center space-x-2">
                            <div class="w-8 h-8 rounded-full bg-orange-500 flex items-center justify-center text-white font-semibold">JS</div>
                            <span class="hidden md:inline text-gray-700">João Silva</span>
                            <i class="fas fa-chevron-down text-xs text-gray-500"></i>
                        </button>
                        <div class="dropdown-menu absolute hidden right-0 bg-white mt-2 py-2 w-48 rounded-md shadow-lg z-50">
                            <a href="#" class="block px-4 py-2 text-gray-700 hover:bg-orange-50 hover:text-orange-500">Minha Conta</a>
                            <a href="#" class="block px-4 py-2 text-gray-700 hover:bg-orange-50 hover:text-orange-500">Configurações</a>
                            <a href="#" class="block px-4 py-2 text-gray-700 hover:bg-orange-50 hover:text-orange-500">Sair</a>
                        </div>
                    </div>
                    <button id="mobile-menu-button" class="md:hidden text-gray-600">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="mobile-menu hidden md:hidden bg-white py-2 px-4 shadow-md">
            <div class="flex flex-col space-y-3">
                <a href="#" class="text-gray-700 hover:text-orange-500 py-2 border-b border-gray-100">Início</a>
                <a href="#" class="text-gray-700 hover:text-orange-500 py-2 border-b border-gray-100">Conta</a>
                <a href="#" class="text-gray-700 hover:text-orange-500 py-2 border-b border-gray-100">Cartões</a>
                <a href="#" class="text-gray-700 hover:text-orange-500 py-2 border-b border-gray-100">Investimentos</a>
                <a href="#" class="text-gray-700 hover:text-orange-500 py-2">Ajuda</a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-8">
        <div class="flex flex-col lg:flex-row gap-8">
            <!-- Left Sidebar -->
            <div class="lg:w-1/4">
                <!-- Balance Card -->
                <div class="bg-white rounded-xl shadow-sm p-6 mb-6">
                    <h3 class="text-gray-500 text-sm font-medium mb-2">Saldo disponível</h3>
                    <p class="text-3xl font-bold text-gray-800 mb-4">R$ 12.459,23</p>
                    <div class="flex justify-between text-sm">
                        <span class="text-gray-500">Conta: 12345-6</span>
                        <span class="text-gray-500">Ag: 0001</span>
                    </div>
                </div>
                
                <!-- Quick Actions -->
                <div class="bg-white rounded-xl shadow-sm p-6 mb-6">
                    <h3 class="text-lg font-semibold text-gray-800 mb-4">Ações rápidas</h3>
                    <div class="grid grid-cols-2 gap-3">
                        <button class="flex flex-col items-center justify-center p-3 rounded-lg bg-orange-50 text-orange-500 hover:bg-orange-100">
                            <i class="fas fa-exchange-alt text-xl mb-2"></i>
                            <span class="text-sm">Transferir</span>
                        </button>
                        <button class="flex flex-col items-center justify-center p-3 rounded-lg bg-green-50 text-green-500 hover:bg-green-100">
                            <i class="fas fa-barcode text-xl mb-2"></i>
                            <span class="text-sm">Pagar</span>
                        </button>
                        <button class="flex flex-col items-center justify-center p-3 rounded-lg bg-orange-50 text-orange-500 hover:bg-orange-100">
                            <i class="fas fa-money-bill-wave text-xl mb-2"></i>
                            <span class="text-sm">Depositar</span>
                        </button>
                        <button class="flex flex-col items-center justify-center p-3 rounded-lg bg-green-50 text-green-500 hover:bg-green-100">
                            <i class="fas fa-credit-card text-xl mb-2"></i>
                            <span class="text-sm">Cartões</span>
                        </button>
                    </div>
                </div>
                
                <!-- Credit Card -->
                <div class="bg-gradient-to-r from-orange-500 to-green-500 rounded-xl shadow-sm p-6 text-white">
                    <div class="flex justify-between items-start mb-8">
                        <div>
                            <p class="text-sm opacity-80">Cartão de crédito</p>
                            <p class="font-medium">João Silva</p>
                        </div>
                        <img src="https://via.placeholder.com/40x25" alt="Mastercard" class="h-6">
                    </div>
                    <div class="mb-6">
                        <p class="text-sm opacity-80">Número do cartão</p>
                        <p class="text-xl tracking-widest">•••• •••• •••• 1234</p>
                    </div>
                    <div class="flex justify-between">
                        <div>
                            <p class="text-sm opacity-80">Validade</p>
                            <p>12/25</p>
                        </div>
                        <div>
                            <p class="text-sm opacity-80">CVV</p>
                            <p>•••</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Main Content Area -->
            <div class="lg:w-3/4">
                <!-- Welcome Banner -->
                <div class="primary-bg rounded-xl shadow-sm p-6 text-white mb-6">
                    <h2 class="text-2xl font-bold mb-2">Olá, João Silva!</h2>
                    <p class="opacity-90">Bem-vindo de volta ao SeridoPay. Aqui está o resumo das suas atividades recentes.</p>
                </div>
                
                <!-- Transactions -->
                <div class="bg-white rounded-xl shadow-sm p-6 mb-6">
                    <div class="flex justify-between items-center mb-6">
                        <h3 class="text-lg font-semibold text-gray-800">Últimas transações</h3>
                        <a href="#" class="text-orange-500 hover:text-orange-600 text-sm font-medium">Ver todas</a>
                    </div>
                    
                    <div class="space-y-4">
                        <!-- Transaction 1 -->
                        <div class="flex items-center justify-between p-3 hover:bg-gray-50 rounded-lg">
                            <div class="flex items-center">
                                <div class="w-10 h-10 rounded-full bg-orange-100 text-orange-500 flex items-center justify-center mr-3">
                                    <i class="fas fa-shopping-bag"></i>
                                </div>
                                <div>
                                    <p class="font-medium text-gray-800">Amazon.com</p>
                                    <p class="text-sm text-gray-500">12/06/2023 - 14:32</p>
                                </div>
                            </div>
                            <div class="text-right">
                                <p class="font-medium text-red-500">- R$ 249,90</p>
                                <p class="text-sm text-gray-500">Cartão final 1234</p>
                            </div>
                        </div>
                        
                        <!-- Transaction 2 -->
                        <div class="flex items-center justify-between p-3 hover:bg-gray-50 rounded-lg">
                            <div class="flex items-center">
                                <div class="w-10 h-10 rounded-full bg-green-100 text-green-500 flex items-center justify-center mr-3">
                                    <i class="fas fa-arrow-down"></i>
                                </div>
                                <div>
                                    <p class="font-medium text-gray-800">Depósito recebido</p>
                                    <p class="text-sm text-gray-500">10/06/2023 - 08:15</p>
                                </div>
                            </div>
                            <div class="text-right">
                                <p class="font-medium text-green-500">+ R$ 5.000,00</p>
                                <p class="text-sm text-gray-500">Transferência</p>
                            </div>
                        </div>
                        
                        <!-- Transaction 3 -->
                        <div class="flex items-center justify-between p-3 hover:bg-gray-50 rounded-lg">
                            <div class="flex items-center">
                                <div class="w-10 h-10 rounded-full bg-orange-100 text-orange-500 flex items-center justify-center mr-3">
                                    <i class="fas fa-utensils"></i>
                                </div>
                                <div>
                                    <p class="font-medium text-gray-800">Restaurante Sabor</p>
                                    <p class="text-sm text-gray-500">09/06/2023 - 19:45</p>
                                </div>
                            </div>
                            <div class="text-right">
                                <p class="font-medium text-red-500">- R$ 87,50</p>
                                <p class="text-sm text-gray-500">Cartão final 1234</p>
                            </div>
                        </div>
                        
                        <!-- Transaction 4 -->
                        <div class="flex items-center justify-between p-3 hover:bg-gray-50 rounded-lg">
                            <div class="flex items-center">
                                <div class="w-10 h-10 rounded-full bg-green-100 text-green-500 flex items-center justify-center mr-3">
                                    <i class="fas fa-piggy-bank"></i>
                                </div>
                                <div>
                                    <p class="font-medium text-gray-800">Rendimento CDI</p>
                                    <p class="text-sm text-gray-500">05/06/2023 - 00:00</p>
                                </div>
                            </div>
                            <div class="text-right">
                                <p class="font-medium text-green-500">+ R$ 32,15</p>
                                <p class="text-sm text-gray-500">Investimentos</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Investments -->
                <div class="bg-white rounded-xl shadow-sm p-6">
                    <div class="flex justify-between items-center mb-6">
                        <h3 class="text-lg font-semibold text-gray-800">Seus investimentos</h3>
                        <a href="#" class="text-orange-500 hover:text-orange-600 text-sm font-medium">Ver todos</a>
                    </div>
                    
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                        <!-- Investment 1 -->
                        <div class="card-hover bg-gray-50 rounded-lg p-4">
                            <div class="flex justify-between items-start mb-3">
                                <div>
                                    <p class="font-medium text-gray-800">CDB</p>
                                    <p class="text-sm text-gray-500">Banco SeridoPay</p>
                                </div>
                                <div class="bg-green-100 text-green-800 text-xs px-2 py-1 rounded-full">102% CDI</div>
                            </div>
                            <p class="text-2xl font-bold text-gray-800 mb-1">R$ 8.450,00</p>
                            <p class="text-sm text-gray-500">Rendimento: R$ 32,15 (último mês)</p>
                        </div>
                        
                        <!-- Investment 2 -->
                        <div class="card-hover bg-gray-50 rounded-lg p-4">
                            <div class="flex justify-between items-start mb-3">
                                <div>
                                    <p class="font-medium text-gray-800">Tesouro IPCA+</p>
                                    <p class="text-sm text-gray-500">Tesouro Direto</p>
                                </div>
                                <div class="bg-green-100 text-green-800 text-xs px-2 py-1 rounded-full">IPCA + 5,74%</div>
                            </div>
                            <p class="text-2xl font-bold text-gray-800 mb-1">R$ 3.200,00</p>
                            <p class="text-sm text-gray-500">Vencimento: 15/08/2026</p>
                        </div>
                        
                        <!-- Investment 3 -->
                        <div class="card-hover bg-gray-50 rounded-lg p-4">
                            <div class="flex justify-between items-start mb-3">
                                <div>
                                    <p class="font-medium text-gray-800">Fundo Imobiliário</p>
                                    <p class="text-sm text-gray-500">HGLG11</p>
                                </div>
                                <div class="bg-orange-100 text-orange-800 text-xs px-2 py-1 rounded-full">DY 8,5%</div>
                            </div>
                            <p class="text-2xl font-bold text-gray-800 mb-1">R$ 1.750,00</p>
                            <p class="text-sm text-gray-500">Dividendos: R$ 14,87 (último mês)</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white pt-12 pb-8 mt-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-12">
                <div>
                    <h3 class="text-xl font-bold mb-4">
                        <span class="text-orange-500">SERIDO</span><span class="text-white">PAY</span>
                    </h3>
                    <p class="text-gray-400 mb-4">O banco digital feito para você conquistar sua liberdade financeira.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-orange-500"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-gray-400 hover:text-orange-500"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-gray-400 hover:text-orange-500"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-gray-400 hover:text-orange-500"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4">Produtos</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Conta Digital</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Cartão de Crédito</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Empréstimos</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Investimentos</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Seguros</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4">Ajuda</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Central de Ajuda</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Perguntas Frequentes</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Tarifas</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Termos de Uso</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-orange-500">Política de Privacidade</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4">Contato</h4>
                    <ul class="space-y-2 text-gray-400">
                        <li class="flex items-start">
                            <i class="fas fa-map-marker-alt mt-1 mr-3"></i>
                            <span>Av. Seridó, 1000<br>Natal - RN, 59000-000</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone-alt mr-3"></i>
                            <span>0800 123 4567</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope mr-3"></i>
                            <span>contato@seridopay.com.br</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-700 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <p class="text-gray-400 mb-4 md:mb-0">© 2023 SeridoPay. Todos os direitos reservados.</p>
                    <div class="flex space-x-6">
                        <img src="https://via.placeholder.com/40x25" alt="Visa" class="h-6">
                        <img src="https://via.placeholder.com/40x25" alt="Mastercard" class="h-6">
                        <img src="https://via.placeholder.com/40x25" alt="American Express" class="h-6">
                        <img src="https://via.placeholder.com/40x25" alt="Pix" class="h-6">
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        document.getElementById('mobile-menu-button').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        // Dropdown Menu
        const dropdowns = document.querySelectorAll('.dropdown');
        dropdowns.forEach(dropdown => {
            const button = dropdown.querySelector('button');
            const menu = dropdown.querySelector('.dropdown-menu');
            
            button.addEventListener('click', function() {
                menu.classList.toggle('hidden');
            });
            
            // Close when clicking outside
            document.addEventListener('click', function(event) {
                if (!dropdown.contains(event.target)) {
                    menu.classList.add('hidden');
                }
            });
        });

        // Card hover effect
        const cards = document.querySelectorAll('.card-hover');
        cards.forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-5px)';
                this.style.boxShadow = '0 10px 25px rgba(0, 0, 0, 0.1)';
            });
            
            card.addEventListener('mouseleave', function() {
                this.style.transform = '';
                this.style.boxShadow = '';
            });
        });

        // Simulate loading
        document.addEventListener('DOMContentLoaded', function() {
            setTimeout(() => {
                document.body.classList.remove('opacity-0');
            }, 100);
        });
    </script>
</body>
</html>
