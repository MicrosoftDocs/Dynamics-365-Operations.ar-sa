---
title: إعداد موارد Azure للفوترة الإلكترونية
description: يوفر هذا الموضوع نظرة عامة حول عملية إعداد موارد Microsoft Azure للفوترة الإلكترونية.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cb1fcddce1054aebf9ef70ba69eb7aca98093cbe
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371479"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>إعداد موارد Azure للفوترة الإلكترونية

[!include [banner](../includes/banner.md)]

تتكون عملية إعداد موارد Microsoft Azure للفوترة الإلكترونية من ثلاث خطوات. تعتبر الخطوتان الأوليتان، "إنشاء مخزن مفاتيح Azure في مدخل Azure" و "إنشاء حساب تخزين Azure في مدخل Azure"، إلزاميتين. الخطوة الثالثة، "تكوين اتصال SharePoint"، اختيارية.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>إنشاء المخزن الرئيسي في Azure في مدخل Azure

أنشئ مخزنًا رئيسيًا في اشتراك Azure. نوصيك بإنشاء مخزن مفاتيح منفصل للفواتير الإلكترونية، وألا تدمج الأسرار مع التطبيقات الأخرى. قم بإنشاء العديد من الأسرار والشهادات التي تريدها لسيناريوهاتك في المستندات الإلكترونية. يجب عليك إنشاء سر واحد على الأقل لتخزين رمز توقيع الوصول المشترك (SAS) لحساب تخزين Azure الذي ستنشئه في الخطوة التالية.

للحصول على معلومات حول كيفية إكمال هذه الخطوة، راجع [إنشاء مخزن رئيسي في Azure في مدخل Azure](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>إنشاء حساب تخزين Azure في مدخل Azure

أنت تمتلك جميع المستندات والملفات الإلكترونية التي يتم إنشاؤها بواسطة خدمة الفواتير الإلكترونية أو الدخول إلى الخدمة. يتم تخزين هذه المستندات والملفات في حساب تخزين Azure الذي تقوم بإنشائه في اشتراك Azure الخاص بك. ستصل الخدمة إلى حساب التخزين الخاص بك باستخدام رمز SAS المأخوذ من سر المخزن الرئيسي الخاص بك.

للحصول على معلومات حول كيفية إكمال هذه الخطوة، راجع [إنشاء حساب تخزين Azure في مدخل Azure](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>تكوين اتصال SharePoint

في بعض السيناريوهات، قد تضطر إلى حفظ الملفات الإلكترونية في SharePoint واستردادها من SharePoint. للتأكد من أن خدمة الفواتير الإلكترونية يمكنها الوصول إلى مجلدات SharePoint، قم بتكوين الوصول إلى SharePoint.

لمزيد من المعلومات حول كيفيه إكمال هذه الخطوة، راجع [تكوين اتصال SharePoint](e-invoicing-create-sharepoint-connection.md).