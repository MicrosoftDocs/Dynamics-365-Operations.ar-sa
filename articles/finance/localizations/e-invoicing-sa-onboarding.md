---
title: إعداد الفواتير الإلكترونية في المملكة العربية السعودية
description: تشرح هذه المقالة كيفية إشراك دافعي الضرائب وبرامج الفواتير الإلكترونية الخاصة بهم مع سلطات الضرائب في المملكة العربية السعودية.
author: mrolecki
ms.date: 06/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Saudi Arabia
ms.author: mrolecki
ms.search.validFrom: 2022-07-15
ms.dyn365.ops.version: AX 10.0.28
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 63bf4d1566849bdff74604f5542634bfd580cd1c
ms.sourcegitcommit: 61be5f43c9678e9f12b4a90410876b4a179ac585
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427092"
---
# <a name="electronic-invoicing-onboarding-in-saudi-arabia"></a>إعداد الفواتير الإلكترونية في المملكة العربية السعودية

[!include [banner](../includes/banner.md)]

يعد الانضمام إلزاميًا لجميع دافعي الضرائب الخاضعين للفواتير الإلكترونية في المملكة العربية السعودية. نتيجة لعملية الإعداد، يحصل دافعو الضرائب على معرّفات طوابع التشفير (CSIDs). مطلوب معرفات CSID للتكامل مع بوابة الفواتير الإلكترونية التي تديرها هيئة الضرائب في المملكة العربية السعودية (ZATCA) ولتقديم المزيد من الفواتير الإلكترونية.

تشرح هذه المقالة كيفية إشراك دافعي الضرائب وبرامج الفواتير الإلكترونية الخاصة بهم مع سلطات الضرائب في المملكة العربية السعودية.

## <a name="prerequisites"></a>المتطلبات الأساسية

- يجب أن يكون الكيان القانوني مسجلاً كدافع ضرائب في المملكة العربية السعودية ويجب أن يكون لديه رقم تسجيل صالح في ضريبة القيمة المضافة (VAT).
- يجب أن يكون للكيان القانوني حق الوصول إلى [بوابة الضرائب في المملكة العربية السعودية (إيراد)](https://fatoora.zatca.gov.sa/).

## <a name="onboarding-process"></a>عملية الإعداد

تتكون عملية الإعداد من خطوتين:

1. الحصول على CSID الامتثال (CCSID)، الذي تعينه ZATCA لإجراء فحوصات الامتثال لحلول إنشاء الفواتير الإلكترونية (EGSs).
2. احصل على CSID الإنتاج (PCSID)، والذي تعينه ZATCA لمعايير EGS المتوافقة.

### <a name="obtain-a-ccsid"></a>الحصول على CCSID

1. في [بوابة الضرائب في المملكة العربية السعودية (ERAD)](https://fatoora.zatca.gov.sa/)، انتقل إلى بوابة Onboarding and Management عن طريق تحديد المربع ذي الصلة.
2. في الصفحة الرئيسية لبوابة Onboarding and Management، حدد **لوحة وحدة / جهاز الحل الجديد Onboard**، ثم حدد **إنشاء رمز OTP**.
3. حدد عدد رموز كلمة المرور لمرة واحدة (OTP) التي تريد إنشاؤها. يعتمد الرقم على عدد وحدات (الأجهزة) إنشاء الفواتير الإلكترونية التي سيتم استخدامها.
4. احفظ رموز OTP التي تم إنشاؤها حتى تتمكن من استخدامها في خطوات لاحقة.
5. قم بإعداد ملف تكوين لطلب توقيع الشهادة. يجب أن يكون ملف التكوين هذا في شكل ملف نص عادي يحتوي على البيانات التالية.

    ```txt
    oid_section = OIDs
    [OIDs]
    certificateTemplateName = 1.3.6.1.4.1.311.20.2
    [req]
    default_bits = 2048
    emailAddress = MyEmail@email.com
    req_extensions = v3_req
    x509_extensions = v3_ca
    prompt = no
    default_md = sha 256
    req_extensions = req_ext
    distinguished_name = dn
    [dn]
    C=SA
    OU=Riyad Branch
    O=Contoso
    CN=EA123456789
    [v3_req]
    basicConstraints = CA:FALSE
    keyUsage = digitalSignature, nonRepudiation, keyEncipherment
    [req_ext]
    certificateTemplateName = ASN1:PRINTABLESTRING:TSTZATCACodeSigning
    subjectAltName = dirName:alt_names
    [alt_names]
    SN=1-TST|2-TST|3-ed22f1d8-e6a2-1118-9b58-d9a8f11e445f
    UID=310122393500003
    title=1100
    registeredAddress= MyAddress
    businessCategory=Industry
    ```

6. في ملف التكوين، قم بتحديث قيمة **عنوان البريد الإلكتروني** والبيانات المحددة التالية.

    | الكود              | ‏‏الوصف‬ | المواصفات |
    |-------------------|-------------|---------------|
    | C                 | رمز البلد / المنطقة. | رمز من حرفين (ISO 3166 Alpha-2) |
    | OU                | اسم الوحدة التنظيمية. | بالنسبة لدافعي الضرائب العاديين، تكون القيمة نصًا مجانيًا. بالنسبة لمجموعات ضريبة القيمة المضافة، حدد القيمة من خلال الرقم الحادي عشر لمعرف المؤسسة على أنه "1". تحقق من أن الإدخال عبارة عن رقم تعريف ضريبي (TIN) مكون من 10 أرقام. |
    | O                 | اسم المنظمة أو دافع الضرائب. | النص الحر |
    | CN                | الاسم الفريد للحل أو الوحدة. | النص الحر |
    | SN                | رمز التعريف الفريد للحل. | النص الحر |
    | المعرف الفريد               | رقم تسجيل ضريبة القيمة المضافة للمكلف. | خمسة عشر رقما. هذا الرقم يبدأ بـ "3" وينتهي بـ "3". |
    | العنوان             | نوع المستند الذي ستصدره وحدة حل دافع الضرائب. | الإدخال العددي المكون من أربعة أرقام والذي يستخدم "0" و"1" معين إلى "TSCZ": 0 = False/Not supported، 1 = True/Supported. T = فاتورة ضريبية (قياسية)، S = فاتورة ضريبية مبسطة، C = للاستخدام المستقبلي، Z = للاستخدام المستقبلي. |
    | registeredAddress | عنوان الفرع أو الموقع الذي يوجد فيه الجهاز أو وحدة الحل بشكل أساسي. | النص الحر |
    | businessCategory  | الصناعة أو القطاع الذي سينشئ الجهاز أو الحل فواتير له. | النص الحر |

7. قم بتشغيل [البرنامج النصي للإعداد](#script) الذي تم توفيره لاحقًا في هذه المقالة. حدد OTP وملف التكوين كمعلمات إدخال. وفيما يلي مثال على ذلك:

    `.\OnboardingScript.ps1 -action getComplianceCSID -otp 123345 -csrconfig .\csr_config.txt -password 123`

    > [!NOTE]
    > معلمة **كلمة المرور** اختيارية ويمكن حذفها. إذا تم تضمينها، فستحتوي الشهادة التي تم إنشاؤها على كلمة المرور المحددة.

8. يتم استلام CCSID كملف شهادة بتنسيق PFX. احفظ ملف شهادة CCSID هذا في مخزن المفاتيح من Microsoft Azure. لمزيد من المعلومات، راجع [شهادات العملاء والأسرار](e-invoicing-customer-certificates-secrets.md).
9. قم بتكوين إعداد الميزة ذات الصلة في ميزة **الفوترة الإلكترونية للفاتورة الإلكترونية في المملكة العربية السعودية (SA)**، وقم بالرجوع إلى شهادة CCSID التي قمت بحفظها في خزنة المفاتيح. سيتم استخدام الشهادة للتواصل مع بوابة الفواتير الإلكترونية ZATCA.

### <a name="obtain-a-pcsid"></a>الحصول على PCSID

للحصول على PCSID، يجب عليك تكوين الحل بشكل صحيح لإنشاء الفاتورة الإلكترونية وإرسالها، ويجب أن يعمل الحل بشكل كامل. لتحقيق هذه النتيجة، يجب عليك إكمال جميع خطوات التكوين الأولية المطلوبة. لمزيد من المعلومات، راجع [بدء استخدام الفواتير الإلكترونية للمملكة العربية السعودية](e-invoicing-sa-get-started.md).

للتحقق من الامتثال، قم بإنشاء جميع أنواع نماذج الفواتير التي تخطط لإصدارها، بناءً على احتياجات عملك، وأرسلها إلى ZATCA. استخدم العملية القياسية لإصدار الفواتير الإلكترونية. لمزيد من المعلومات، راجع [إصدار الفواتير الإلكترونية في Finance and Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md).

> [!NOTE]
> بالإضافة إلى الفواتير، يجب عليك إنشاء وتقديم نماذج إشعار دائن وإشعارات خصم عند حصولك على PCSID لتسجيل جميع أنواع المستندات التي قد يتم إصدارها.

1. تأكد من إرسال جميع الفواتير الإلكترونية بنجاح إلى ZATCA.
2. قم بتشغيل [البرنامج النصي للإعداد](#script) الذي تم توفيره لاحقًا في هذه المقالة. حدد CCSID كمعامل إدخال. وفيما يلي مثال على ذلك:

    `.\OnboardingScript.ps1 -action getProductionCSID -password 123`

    > [!NOTE]
    > معلمة **كلمة المرور** اختيارية ويمكن حذفها. إذا تم تضمينها، فستحتوي الشهادة التي تم إنشاؤها على كلمة المرور المحددة.

3. يتم استلام PCSID كملف شهادة بتنسيق PFX. احفظ ملف شهادة PCSID هذا في خزنة المفاتيح.
4. قم بتكوين إعداد الميزة ذات الصلة في ميزة الفوترة الإلكترونية **للفاتورة الإلكترونية في المملكة العربية السعودية (SA)**. استبدل شهادة CCSID التي تم تكوينها مسبقًا بشهادة CCSID التي تم الحصول عليها والتي حفظتها في مخزن المفاتيح.

بعد إكمال جميع خطوات التهيئة، يصبح النظام جاهزًا للاستخدام في وضع الإنتاج.

لمراجعة معرفات CSID التي تم الحصول عليها من جانب ZATCA، استخدم **مربع مراجعة معرّف طوابع التشفير الحالي (CSID)** على الصفحة المقصودة لبوابة Onboarding والإدارة. يمكن الوصول إلى هذه البوابة من البوابة الرئيسية [للضرائب في المملكة العربية السعودية (ERAD)](https://fatoora.zatca.gov.sa/).

## <a name="onboarding-script"></a><a id="script"></a>تأهيل البرنامج النصي

> [!NOTE]
> نماذج البرامج النصية غير مدعومة ضمن أي برنامج أو خدمة دعم قياسية من Microsoft. يتم توفير نماذج البرامج النصية كما هي دون أي ضمان من أي نوع. كما تخلي Microsoft مسؤوليتها عن جميع الضمانات الضمنية بما في ذلك، على سبيل المثال لا الحصر، أي ضمانات ضمنية خاصة بالتسويق أو الملاءمة لغرض معين. تظل المخاطر الكاملة الناشئة عن استخدام أو أداء نماذج البرامج النصية والوثائق معك. لا تتحمل Microsoft أو مؤلفوها أو أي شخص آخر مشارك في إنشاء البرامج النصية أو إنتاجها أو تسليمها بأي حال من الأحوال المسؤولية عن أي أضرار من أي نوع (بما في ذلك، على سبيل المثال لا الحصر، الأضرار الناجمة عن فقدان أرباح الأعمال، أو انقطاع العمل، أو فقدان معلومات العمل، أو أي خسارة مالية أخرى) تنشأ عن استخدام أو عدم القدرة على استخدام نماذج البرامج النصية أو الوثائق، حتى إذا تم إخطار Microsoft بإمكانية حدوث مثل هذه الأضرار.

1. استخدم برنامج Windows PowerShell النصي التالي للحصول على CCSID وPCSID.

    ```powershell
    param($action, $otp, $csrconfig, $password)
    $env:path = $env:path + ";C:\Program Files\Git\usr\bin"
    
    if ($action -eq "getComplianceCSID")
    {
        if (-not (Test-Path -Path $csrconfig))
        {
            throw "CSR configuration file does not exist, please make sure to provide a valid file path for the '-csrconfig' parameter."
        }

        if ($otp -eq $null)
        {
            throw "OTP code is not provided, please carry correct parameters."
        }

        #Generate private key
        openssl ecparam -name secp256k1 -genkey -noout -out privatekey.pem
        Write-Host "Private key generated."

        #Generate public key
        openssl ec -in privatekey.pem -pubout -conv_form compressed -out publickey.pem
        Write-Host "Public key generated."

        #Generate CSR(Certificate signing request)
        openssl base64 -d -in publickey.pem -out publickey.bin
        openssl req -new -sha256 -key privatekey.pem -extensions v3_req -config $csrconfig -out .\taxpayer.csr 
        openssl base64 -in taxpayer.csr -out taxpayerCSRbase64Encoded.txt
        $CSRbase64Encoded = Get-Content -path taxpayerCSRbase64Encoded.txt -Raw
        $CSRbase64Encoded = $CSRbase64Encoded -replace "`n",""
        $CSRbase64Encoded = $CSRbase64Encoded -replace "`r",""

        #Init request for CCSID
        $postParams = @{"csr"=$CSRbase64Encoded} | ConvertTo-Json
        $postHeader = @{
               "Accept"="application/json"
               "OTP"=$otp
               "Content-Type"="application/json"}

        try
        {
            #Change URL to Zatca production URL when officially onboarding
            $response = Invoke-WebRequest -Uri 'https://gw-apic-gov.gazt.gov.sa/e-invoicing/developer-portal/compliance' -Method POST -Body $postParams -Headers $postHeader 
        }
        catch
        {
            Write-Host "Zatca service communication error:"
            Write-Host $_.Exception.Message 
            Write-Host "Please make sure the OTP code in script parameter and Serial Number (SN) in configuration file are valid."
            Write-Host "The process of obtaining a Compliance CSID (CCSID) is interrupted."
        }

        if ($response -ne $null)
        {
            $response = $response | ConvertFrom-Json
            $requestId = $response.requestID
            Write-Host "Request ID:"
            Write-Host $requestId
            $requestId | Out-File -FilePath .\requestId.txt -Encoding utf8 -NoNewline

            $CCSIDbase64 = $response.binarySecurityToken
            Write-Host "Compliance CSID received from Zatca:"
            Write-Host $CCSIDbase64
            $CCSID = [System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String($CCSIDbase64))
            $CCSIDCertString = "-----BEGIN CERTIFICATE-----`n" + $CCSID + "`n" + "-----END CERTIFICATE-----"

            $CCSIDStringFileName = "CCSIDString.txt"
            $CCSIDCertFileName = "CCSID.pem"
            $CCSIDFolderPath = Get-Location
            $CCSIDCertFilePath = Join-Path $CCSIDFolderPath $CCSIDCertFileName
            $CCSIDStringFilePath = Join-Path $CCSIDFolderPath $CCSIDStringFileName

            $Utf8NoBomEncoding = New-Object System.Text.UTF8Encoding $False
            [System.IO.File]::WriteAllLines($CCSIDCertFilePath, $CCSIDCertString, $Utf8NoBomEncoding)
            [System.IO.File]::WriteAllLines($CCSIDStringFilePath, $CCSIDbase64, $Utf8NoBomEncoding)

            openssl pkcs12 -inkey privatekey.pem -in CCSID.pem -export -passout pass:$password -out CCSID.pfx
            Write-Host "Certificate is saved to CCSID.pfx file."
            Write-Host "The process of obtaining a Compliance CSID (CCSID) is complete, please process the compliance check and do not delete or move any created files before getting PCSID."
        }

    }


    if ($action -eq "getProductionCSID")
    {
        if (-not (Test-Path -Path requestId.txt))
        {
            throw "'requestId.txt' file is missing, please make sure you're running the script in the same location where the results of getting the CCSID are stored."
        }
        if (-not (Test-Path -Path CCSIDString.txt))
        {
            throw "'CCSIDString.txt' file is missing, please make sure you're running the script in the same location where the results of getting the CCSID are stored."
        }

        $requestId = Get-Content -path requestId.txt -Raw
        $requestId = $requestId -replace "`n",""
        $requestId = $requestId -replace "`r",""
        Write-Host "Request ID for PCSID is:" $requestId
        $CCSID = Get-Content -path CCSIDString.txt -Raw
        $CCSID = $CCSID -replace "`n",""
        $CCSID = $CCSID -replace "`r",""
        Write-Host "Compliance CSID received from Zatca:"
        Write-Host $CCSID

        #Init request for Production CSID (PCSID)
        $postParams = @{"compliance_request_id"=$requestId} | ConvertTo-Json
        $postHeader = @{
               "Accept"="application/json"
               "currentCCSID"=$CCSID
               "Content-Type"="application/json"}

        try
        {
            #Change URL to Zatca production URL when officially onboarding
            $response = Invoke-WebRequest -Uri 'https://gw-apic-gov.gazt.gov.sa/e-invoicing/developer-portal/production/csids' -Method POST -Body $postParams -Headers $postHeader
        }
        catch
        {
            Write-Host "Zatca service communication error:"
            Write-Host $_.Exception.Message 
            Write-Host "Please make sure the compliance check process has been done before obtaining a Production CSID (PCSID)."
            Write-Host "The process of obtaining a Production CSID (PCSID) is interrupted."
        }

        if ($response -ne $null)
        {
            $response = $response | ConvertFrom-Json
            $PCSIDbase64 = $response.binarySecurityToken
            Write-Host "Production CSID received from Zatca:"
            Write-Host $PCSIDbase64

            $PCSID = [System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String($PCSIDbase64))
            $PCSIDCertString = "-----BEGIN CERTIFICATE-----`n" + $PCSID + "`n" + "-----END CERTIFICATE-----"

            $PCSIDCertFileName = "PCSID.pem"
            $PCSIDCertFilePath = Get-Location
            $PCSIDCertFilePath = Join-Path $PCSIDCertFilePath $PCSIDCertFileName

            $Utf8NoBomEncoding = New-Object System.Text.UTF8Encoding $False
            [System.IO.File]::WriteAllLines($PCSIDCertFilePath, $PCSIDCertString, $Utf8NoBomEncoding)

            # Sandbox API will get error: openssl : No certificate matches private key
            openssl pkcs12 -inkey privatekey.pem -in PCSID.pem -export -passout pass:$password -out PCSID.pfx

            if (Test-Path -Path PCSID.pfx)
            {
                Write-Host "Certificate is saved to PCSID.pfx file."
                Write-Host "The process of obtaining a Production CSID (PCSID) is complete."
            }
            else
            {
                Write-Host "The process of obtaining a Production CSID (PCSID) is interrupted."
            }
        }
    } 
    ```

2. احفظ ملف شهادة .pfx الناتج الذي تم استلامه في خزنة المفاتيح.

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على الفوترة الإلكترونية](e-invoicing-service-overview.md)
- [الشروع في العمل مع إدارة خدمة الفوترة الإلكترونية](e-invoicing-get-started-service-administration.md)
- [الشروع في العمل باستخدام الفوترة الإلكترونية](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
