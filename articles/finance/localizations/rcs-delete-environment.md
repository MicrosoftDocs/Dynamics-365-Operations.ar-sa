---
title: Regulatory Configuration Service (RCS) - حذف بيئة RCS
description: توضح هذه المقالة كيف يمكن لمسؤول نظام Regulatory Configuration Service‏ (RCS) حذف بيئة RCS والبيانات ذات الصلة.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 21e7ee546bb2b712d9424c6bd95e9f9227831bd1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908879"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - حذف بيئة RCS

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيف يمكن لمسؤول نظام Regulatory Configuration Service‏ (RCS) حذف بيئة RCS والبيانات ذات الصلة.

قبل أن تتمكن من استكمال الإجراء في هذه المقالة، يجب تلبية المتطلبات التالية:

- يجب تعيين دور **مسؤول النظام** لك لبيئة RCS.
- يجب أن يحتوي دور **مسؤول النظام** على دور **RCSDeleteEnvironmentDuty** معين إليه.

## <a name="delete-an-rcs-environment"></a>حذف بيئة RCS

1. افتح RCS، وحدد لوحة مساحة عمل **التقارير الإلكترونية**.
2. في القسم **ارتباطات ذات صلة**، حدد **حذف بيئة RCS**.

    ![حذف ارتباط بيئة RCS في قسم ارتباطات ذات صلة.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. في مربع الحوار الذي يظهر، راجع الرسائل حول نطاق حذف البيئة.

    ![الرسائل الموجودة في مربع الحوار حذف بيئة RCS.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > لا يمكن عكس حذف بيئة RCS.
    >
    > تقوم العملية بحذف بيئة RCS المحددة وأية بيانات مرتبطة، بما في ذلك الميزات والتكوينات المخزنة في المستودع العالمي. لن يتم إلغاء مشاركة الميزات والتكوينات المشتركة مع المؤسسات الأخرى ويتم حذفها إذا لم يكن لديها تبعيات. سيتم وضع علامة موقوف على الميزات والتكوينات التي لها تبعيات.

4. في الحقل الذي يتم توفيره، أدخل المعرّف الفريد العمومي (GUID) الخاص ببيئة RCS لتأكيد رغبتك في حذفه. يتم تضمين المعرّف الفريد العمومي (GUID) الخاص بالبيئة في رسالة الحذف.
5. حدد **حذف البيئة**.
    
يتم الآن حذف بيئة RCS الخاصة بك وأية بيانات مرتبطة.

> [!IMPORTANT]
> بعد حذف بيئة RCS، لا توجد طريقة لاسترداد البيانات. يمكن إنشاء بيئة RCS جديدة في أي منطقة RCS متوفرة.
