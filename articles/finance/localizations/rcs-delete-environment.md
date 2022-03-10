---
title: Regulatory Configuration Service (RCS) - حذف بيئة RCS
description: يشرح هذا الموضوع كيف يمكن لمسؤول نظام Regulatory Configuration Service (RCS) حذف بيئة RCS والبيانات ذات الصلة.
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
ms.openlocfilehash: f9073a14143423676f23f9bf8dc9c17dbae18a6c3ad0d2f6d1e33919fd9162bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759809"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - حذف بيئة RCS

[!include [banner](../includes/banner.md)]

يشرح هذا الموضوع كيف يمكن لمسؤول نظام Regulatory Configuration Service (RCS) حذف بيئة RCS والبيانات ذات الصلة.

قبل أن تتمكن من استكمال الإجراء في هذا الموضوع، يجب تلبية المتطلبات التالية:

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
