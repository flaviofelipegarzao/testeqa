*** Settings ***
Library    SeleniumLibrary


    Open Browser    ${URL}    ${BROWSER}
    Maximize Browser Window
    Click Element    xpath=//a[contains(text(),'Sign in')]
    Input Text       xpath=//input[@id='email_create']    ${EMAIL}
    Click Element    xpath=//button[@id='SubmitCreate']
    Wait Until Element Is Visible    xpath=//input[@id='customer_firstname']    timeout=10s
    Input Text       xpath=//input[@id='customer_firstname']    Test
    Input Text       xpath=//input[@id='customer_lastname']    User
    Input Text       xpath=//input[@id='passwd']    ${PASSWORD}
    Click Element    xpath=//button[@id='submitAccount']
    Wait Until Element Is Visible    xpath=//a[@class='account']    timeout=10s
    Page Should Contain Element    xpath=//a[@class='account']
    Capture Page Screenshot
    Close Browser

Logout Da Conta
    Open Browser    ${URL}    ${BROWSER}
    Maximize Browser Window
    Click Element    xpath=//a[contains(text(),'Sign in')]
    Input Text       xpath=//input[@id='email']    ${EMAIL}
    Input Text       xpath=//input[@id='passwd']    ${PASSWORD}
    Click Element    xpath=//button[@id='SubmitLogin']
    Wait Until Element Is Visible    xpath=//a[@class='logout']    timeout=10s
    Click Element    xpath=//a[@class='logout']
    Wait Until Element Is Visible    xpath=//input[@id='email']    timeout=10s
    Page Should Contain Element    xpath=//input[@id='email']
    Capture Page Screenshot
    Close Browser

Cadastro Com Campos Vazios
    Open Browser    ${URL}    ${BROWSER}
    Maximize Browser Window
    Click Element    xpath=//a[contains(text(),'Sign in')]
    Click Element    xpath=//button[@id='SubmitCreate']
    Wait Until Element Is Visible    xpath=//div[contains(@class,'alert-danger')]    timeout=10s
    Page Should Contain    There are errors
    Capture Page Screenshot
    Close Browser
