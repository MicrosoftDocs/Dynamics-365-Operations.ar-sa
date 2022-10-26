---
title: تثبيت حل Invoice capture
description: توفر هذه المقالة معلومات حول كيفية تثبيت حل التقاط الفاتورة ودمجها معه Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691122"
---
# <a name="install-the-invoice-capture-solution"></a>تثبيت حل Invoice capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> إذا قمت بتثبيت الحل في المعاينة الخاصة ، يجب عليك إلغاء تثبيت الحل القديم قبل المتابعة.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل أن تتمكن من تثبيت حل Invoice capture، يجب عليك إكمال المتطلبات الأساسية التالية:

1. قم بتسجيل تطبيق وإضافة سر عميل إلى Microsoft Azure Active Directory (Azure AD) ضمن اشتراك Azure. لمزيد من المعلومات، راجع [قم بتسجيل تطبيق ويب مع AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > تأكد من تدوين ملاحظة بشأن قيم **معرف التطبيق (العميل)**، و **سر العميل**، و **معرف المستأجر**، لأنك ستحتاج إليها لاحقًا.

2. قم بتسجيل تطبيق Azure في بيئة Dynamics 365 Finance. لمزيد من المعلومات، راجع [سجل طلبك الخارجي](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>قم بتثبيت وإعداد الحل

لتثبيت حل Invoice capture ، انتقل إلى AppSource ، ثم حدد الارتباط الخاص بإصدار المعاينة لإصدار Dynamics 365 Invoice capture [الفواتير](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). بعد اكتمال التثبيت ، ستشاهد الحل المثبت في البيئة المحددة في Power Apps.

لإكمال الإعداد ، اتبع هذه الخطوات.

1. حمل [حل مساعد](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) لإعداد التفاصيل التالية:

    - الاتصال بين Microsoft Power Platform وبيئة التمويل
    - مرجع الاتصال ل Dataverseو Office 365Outlook الذي سيتم استخدامه بواسطة القناة

2. في Power Apps ، انتقل إلى البيئة الخاصة بك ، وحدد **استيراد حل**.
3. حدد **استعراض** ، وحدد حزمه الحلول المساعد التي قمت بتنزيلها ، ثم حدد **التالي**.
4. حدد **التالي**.
5. قم بتعيين اتصال موجود ، أو قم بإنشاء اتصال جديد عن طريق تحديد **اتصال** جديد.
6. بعد استيراد الحزمة بنجاح ، افتح **Dynamics 365 Invoice capture – أدوات** التثبيت.
7. قم بتشغيل تدفق السحابة لاعداد الاتصال بين حل Invoice capture في والمالية Microsoft Power Platform.
8. حدد **تشغيل** ، وحدد المحددات التالية:

    - **Url** الخاص ب Dynamics 365 Finance عنوان url الخاص ببيئة التمويل التي ترغب في التكامل معها.
    - **معرف المستأجر** - معرّف المستأجر لبيئة التمويل.
    - **معرف** العميل – معرف تطبيق Azure الذي تم تسجيله.
    - **سر العميل** -سر العميل الذي تم إنشاؤه لتطبيق Azure.
