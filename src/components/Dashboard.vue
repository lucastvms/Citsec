<template>
	<div class="grid">
		<div class="col-12 lg:col-6 xl:col-3">
			<div class="card mb-0">
				<div class="flex justify-content-between mb-3">
					<div>
						<span class="block text-500 font-medium mb-3">Processos mapeados</span>
						<div class="text-900 font-medium text-xl">152</div>
					</div>
					<div class="flex align-items-center justify-content-center bg-blue-100 border-round" style="width:2.5rem;height:2.5rem">
						<!-- <i class="pi pi-shopping-cart text-blue-500 text-xl"></i> -->
					</div>
				</div>
				<span class="text-green-500 font-medium">24 novos </span>
				<span class="text-500">desde o último acesso</span>
			</div>
		</div>
		<div class="col-12 lg:col-6 xl:col-3">
			<div class="card mb-0">
				<div class="flex justify-content-between mb-3">
					<div>
						<span class="block text-500 font-medium mb-3">Gap analysis </span>
						<div class="text-900 font-medium text-xl">7</div>
					</div>
					<div class="flex align-items-center justify-content-center bg-orange-100 border-round" style="width:2.5rem;height:2.5rem">
						<!-- <i class="pi pi-map-marker text-orange-500 text-xl"></i> -->
					</div>
				</div>
				<span class="text-green-500 font-medium">2 </span>
				<span class="text-500">desde a última semana</span>
			</div>
		</div>
		<div class="col-12 lg:col-6 xl:col-3">
			<div class="card mb-0">
				<div class="flex justify-content-between mb-3">
					<div>
						<span class="block text-500 font-medium mb-3">Alto risco</span>
						<div class="text-900 font-medium text-xl">21</div>
					</div>
					<div class="flex align-items-center justify-content-center bg-cyan-100 border-round" style="width:2.5rem;height:2.5rem">
						<!-- <i class="pi pi-inbox text-cyan-500 text-xl"></i> -->
					</div>
				</div>
				<span class="text-green-500 font-medium">3  </span>
				<span class="text-500">novos registros</span>
			</div>
		</div>
		<div class="col-12 lg:col-6 xl:col-3">
			<div class="card mb-0">
				<div class="flex justify-content-between mb-3">
					<div>
						<span class="block text-500 font-medium mb-3">Denúncias</span>
						<div class="text-900 font-medium text-xl">45 </div>
					</div>
					<div class="flex align-items-center justify-content-center bg-purple-100 border-round" style="width:2.5rem;height:2.5rem">
						<!-- <i class="pi pi-comment text-purple-500 text-xl"></i> -->
					</div>
				</div>
				<span class="text-green-500 font-medium">14 </span>
				<span class="text-500">resolvidas</span>
			</div>
		</div>

	<div class="col-12 xl:col-6">
		<!-- <div class="card">
			<h5>Recent Sales</h5>
			<DataTable :value="products" :rows="5" :paginator="true" responsiveLayout="scroll">
				<Column style="width:15%">
					<template #header>
						Image
					</template>
					<template #body="slotProps">
						<img :src="'images/product/' + slotProps.data.image" :alt="slotProps.data.image" width="50" class="shadow-2" />
					</template>
				</Column>
				<Column field="name" header="Name" :sortable="true" style="width:35%"></Column>
				<Column field="price" header="Price" :sortable="true" style="width:35%">
					<template #body="slotProps">
						{{formatCurrency(slotProps.data.price)}}
					</template>
				</Column>
				<Column style="width:15%">
					<template #header>
						View
					</template>
					<template #body>
						<Button icon="pi pi-search" type="button" class="p-button-text"></Button>
					</template>
				</Column>
			</DataTable>
		</div> -->
		<div class="card">
			<div class="flex justify-content-between align-items-center mb-5">
				<h5>Acompanhamentos</h5>
				<div>
					<Button icon="pi pi-ellipsis-v" class="p-button-text p-button-plain p-button-rounded" @click="$refs.menu2.toggle($event)"></Button>
					<Menu ref="menu2" :popup="true" :model="items"></Menu>
				</div>
			</div>
			<ul class="list-none p-0 m-0">
				<li class="flex flex-column md:flex-row md:align-items-center md:justify-content-between mb-4">
					<div>
						<span class="text-900 font-medium mr-2 mb-1 md:mb-0">Treinamentos</span>
						<!-- <div class="mt-1 text-600">Clothing</div> -->
					</div>
					<div class="mt-2 md:mt-0 flex align-items-center">
						<div class="surface-300 border-round overflow-hidden w-10rem lg:w-6rem" style="height:8px">
							<div class="bg-orange-500 h-full" style="width:50%"></div>
						</div>
						<span class="text-orange-500 ml-3 font-medium">%50</span>
					</div>
				</li>
				<li class="flex flex-column md:flex-row md:align-items-center md:justify-content-between mb-4">
					<div>
						<span class="text-900 font-medium mr-2 mb-1 md:mb-0">Gaps</span>
						<!-- <div class="mt-1 text-600">Accessories</div> -->
					</div>
					<div class="mt-2 md:mt-0 ml-0 md:ml-8 flex align-items-center">
						<div class="surface-300 border-round overflow-hidden w-10rem lg:w-6rem" style="height:8px">
							<div class="bg-cyan-500 h-full" style="width:16%"></div>
						</div>
						<span class="text-cyan-500 ml-3 font-medium">%16</span>
					</div>
				</li>
				<li class="flex flex-column md:flex-row md:align-items-center md:justify-content-between mb-4">
					<div>
						<span class="text-900 font-medium mr-2 mb-1 md:mb-0">Plano de ação</span>
						<!-- <div class="mt-1 text-600">Accessories</div> -->
					</div>
					<div class="mt-2 md:mt-0 ml-0 md:ml-8 flex align-items-center">
						<div class="surface-300 border-round overflow-hidden w-10rem lg:w-6rem" style="height:8px">
							<div class="bg-pink-500 h-full" style="width:67%"></div>
						</div>
						<span class="text-pink-500 ml-3 font-medium">%67</span>
					</div>
				</li>
				<li class="flex flex-column md:flex-row md:align-items-center md:justify-content-between mb-4">
					<div>
						<span class="text-900 font-medium mr-2 mb-1 md:mb-0">Gestão de riscos</span>
						<!-- <div class="mt-1 text-600">Office</div> -->
					</div>
					<div class="mt-2 md:mt-0 ml-0 md:ml-8 flex align-items-center">
						<div class="surface-300 border-round overflow-hidden w-10rem lg:w-6rem" style="height:8px">
							<div class="bg-green-500 h-full" style="width:35%"></div>
						</div>
						<span class="text-green-500 ml-3 font-medium">%35</span>
					</div>
				</li>
				<li class="flex flex-column md:flex-row md:align-items-center md:justify-content-between mb-4">
					<div>
						<span class="text-900 font-medium mr-2 mb-1 md:mb-0">Denúncias</span>
						<!-- <div class="mt-1 text-600">Accessories</div> -->
					</div>
					<div class="mt-2 md:mt-0 ml-0 md:ml-8 flex align-items-center">
						<div class="surface-300 border-round overflow-hidden w-10rem lg:w-6rem" style="height:8px">
							<div class="bg-purple-500 h-full" style="width:75%"></div>
						</div>
						<span class="text-purple-500 ml-3 font-medium">%75</span>
					</div>
				</li>
				<!-- <li class="flex flex-column md:flex-row md:align-items-center md:justify-content-between mb-4">
					<div>
						<span class="text-900 font-medium mr-2 mb-1 md:mb-0">Robots T-Shirt</span>
						<div class="mt-1 text-600">Clothing</div>
					</div>
					<div class="mt-2 md:mt-0 ml-0 md:ml-8 flex align-items-center">
						<div class="surface-300 border-round overflow-hidden w-10rem lg:w-6rem" style="height:8px">
							<div class="bg-teal-500 h-full" style="width:40%"></div>
						</div>
						<span class="text-teal-500 ml-3 font-medium">%40</span>
					</div>
				</li> -->
			</ul>	
		</div>
		<div class="card  flex flex-column align-items-center">
				<h5 class="align-self-start">Maturidade de riscos por setor</h5>
				<Chart type="polarArea" :data="polarData" :options="polarOptions" style="width: 50%" />
		</div>
	</div>
	<div class="col-12 xl:col-6">
		<div class="card">
			<h5>Gaps</h5>
			<Chart type="line" :data="lineData" :options="lineOptions" />
		</div>
		<div class="card">
			<div class="flex align-items-center justify-content-between mb-4">
				<h5>Notícias</h5>
				<div>
					<Button icon="pi pi-ellipsis-v" class="p-button-text p-button-plain p-button-rounded" @click="$refs.menu1.toggle($event)"></Button>
					<Menu ref="menu1" :popup="true" :model="items"></Menu>
				</div>
			</div>
			
			<span class="block text-600 font-medium mb-3">HOJE</span>
			<ul class="p-0 mx-0 mt-0 mb-4 list-none">
				<li class="flex align-items-center py-2 border-bottom-1 surface-border">
					<!-- <div class="w-3rem h-3rem flex align-items-center justify-content-center bg-blue-100 border-circle mr-3 flex-shrink-0">
						<i class="pi pi-dollar text-xl text-blue-500"></i>
					</div> -->
					<span class="text-900 line-height-3">
						<span class="text-700">A implementação da <span class="text-blue-500">LGPD</span> no Brasil foi o ponto crucial de consolidação de normas que antes eram fragmentadas em vários códigos brasileiros, 
							como a Constituição, disse o presidente da ANPD.</span>
					</span>
				</li>
				<li class="flex align-items-center py-2">
					<!-- <div class="w-3rem h-3rem flex align-items-center justify-content-center bg-orange-100 border-circle mr-3 flex-shrink-0">
						<i class="pi pi-download text-xl text-orange-500"></i>
					</div> -->
					<span class="text-700 line-height-3">Senado inclui proteção de dados pessoais como direito fundamental.</span>
				</li>
			</ul>

			<span class="block text-600 font-medium mb-3">ONTEM</span>
			<ul class="p-0 m-0 list-none">
				<li class="flex align-items-center py-2 border-bottom-1 surface-border">
					<!-- <div class="w-3rem h-3rem flex align-items-center justify-content-center bg-blue-100 border-circle mr-3 flex-shrink-0">
						<i class="pi pi-dollar text-xl text-blue-500"></i>
					</div> -->
					<span class="text-900 line-height-3">
						<span class="text-700">Começa a valer hoje nova política de privacidade do WhatsApp.</span>
					</span>
				</li>
				<li class="flex align-items-center py-2 border-bottom-1 surface-border">
					<!-- <div class="w-3rem h-3rem flex align-items-center justify-content-center bg-pink-100 border-circle mr-3 flex-shrink-0">
						<i class="pi pi-question text-xl text-pink-500"></i>
					</div> -->
					<span class="text-900 line-height-3">
						<span class="text-700">Punições contra violações da proteção de dados entram em vigor.</span>
					</span>
				</li>
			</ul>
		</div>
		<!-- <div class="px-4 py-5 shadow-2 flex flex-column md:flex-row md:align-items-center justify-content-between mb-3" 
			style="border-radius: 1rem; background: linear-gradient(0deg, rgba(0, 123, 255, 0.5), rgba(0, 123, 255, 0.5)), linear-gradient(92.54deg, #1C80CF 47.88%, #FFFFFF 100.01%)">
			<div>
				<div class="text-blue-100 font-medium text-xl mt-2 mb-3">TAKE THE NEXT STEP</div>
				<div class="text-white font-medium text-5xl">Try PrimeBlocks</div>
			</div> 
		<div class="mt-4 mr-auto md:mt-0 md:mr-0">
				<a href="https://www.primefaces.org/primeblocks-vue" class="p-button font-bold px-5 py-3 p-button-warning p-button-rounded p-button-raised">
					Get Started
				</a>
			</div> 
		</div> -->
	</div>
	</div>
</template>

<script>
import EventBus from '@/AppEventBus';
import ProductService from '../service/ProductService';
// import {radarData, radarOptions} from './ChartDemo.vue';

export default {
	data() {
		return {
			polarData: {
				datasets: [{
					data: [
						11,
						16,
						7,
						3,
						14
					],
					backgroundColor: [
						"#FF6384",
						"#4BC0C0",
						"#FFCE56",
						"#E7E9ED",
						"#36A2EB"
					],
					label: 'My dataset'
				}],
				labels: [
					"Financeiro",
					"RH",
					"TI",
					"Marketing",
					"Jurídico"
				]
			},
			polarOptions: null,
			products: null,
			lineData: {
				labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
				datasets: [
					{
						label: 'Identificados',
						data: [65, 59, 80, 81, 56, 55, 40],
						fill: false,
						backgroundColor: '#2f4860',
						borderColor: '#2f4860',
						tension: 0.4
					},
					{
						label: 'Resolvidos',
						data: [28, 48, 40, 19, 86, 27, 90],
						fill: false,
						backgroundColor: '#00bb7e',
						borderColor: '#00bb7e',
						tension: 0.4
					}
				]
			},
			items: [
                {label: 'Add New', icon: 'pi pi-fw pi-plus'},
                {label: 'Remove', icon: 'pi pi-fw pi-minus'}
            ],
			lineOptions: null,
		}
	},
	productService: null,
	themeChangeListener: null,
	mounted() {
		this.productService.getProductsSmall().then(data => this.products = data);

		this.themeChangeListener = (event) => {
            if (event.dark)
                this.applyDarkTheme();
            else
                this.applyLightTheme();
        };
        EventBus.on('change-theme', this.themeChangeListener);

		if (this.isDarkTheme()) {
            this.applyDarkTheme();
        }
        else {
            this.applyLightTheme();
        }
	},
	beforeUnmount() {
        EventBus.off('change-theme', this.themeChangeListener );
    },
	created() {
		this.productService = new ProductService();
	},
	methods: {
		formatCurrency(value) {
			return value.toLocaleString('en-US', {style: 'currency', currency: 'USD'});
		},
		isDarkTheme() {
            return this.$appState.darkTheme === true;
        },
		applyLightTheme() {
			this.lineOptions = {
				plugins: {
					legend: {
						labels: {
							color: '#495057'
						}
					}
				},
				scales: {
					x: {
						ticks: {
							color: '#495057'
						},
						grid: {
							color:  '#ebedef',
						}
					},
					y: {
						ticks: {
							color: '#495057'
						},
						grid: {
							color:  '#ebedef',
						}
					},
				}
			};
			this.polarOptions = {
				plugins: {
					legend: {
						labels: {
							color: '#495057'
						}
					}
				},
				scales: {
					r: {
						grid: {
							color: '#ebedef'
						}
					}
				}
			};
		},
		applyDarkTheme() {
			this.lineOptions = {
				plugins: {
					legend: {
						labels: {
							color: '#ebedef'
						}
					}
				},
				scales: {
					x: {
						ticks: {
							color: '#ebedef'
						},
						grid: {
							color:  'rgba(160, 167, 181, .3)',
						}
					},
					y: {
						ticks: {
							color: '#ebedef'
						},
						grid: {
							color:  'rgba(160, 167, 181, .3)',
						}
					},
				}
			};
			this.polarOptions = {
				plugins: {
					legend: {
						labels: {
							color: '#ebedef'
						}
					}
				},
				scales: {
					r: {
						grid: {
							color: 'rgba(160, 167, 181, .3)'
						}
					}
				}
			};
		}
	}
}
</script>