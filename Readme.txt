PRIMEIRO TIVE A SEGUINTE IDEIA : 
-  criar um programa para automatizar a inclusão do seu nome em uma lista de presença diariamente em um grupo do WhatsApp, considerando usar um script Python em conjunto com uma biblioteca do Selenium WebDriver, que permite que você automatize ações em um navegador da web.


iNTALEI A BIBLIOTECA NO PIP :

pip install selenium

DEPOIS ESCOLHI O NAVEGADOR FIREFOX POR CONTA QUE ME TESTES O CHROME DEU MUITO PROBLEMA POR CONTA DE VERSÃO




from selenium import webdriver
from selenium.webdriver.firefox.service import Service
rom selenium.webdriver.common.by import By

# caminho para o arquivo do driver do Firefox
driver_path = "C:\Program Files\Mozilla Firefox\geckodriver.exe"

# inicializa o serviço do driver
service = Service(driver_path)

# inicializa o driver do Firefox
driver = webdriver.Firefox(service=service)

# acessa a página do WhatsApp Web
driver.get("https://web.whatsapp.com/")

# buscar elemento na pagina
grupo = driver.find_element(By.XPATH, "//div[@class='teste']")

# entrar no grupo 
grupo.click


