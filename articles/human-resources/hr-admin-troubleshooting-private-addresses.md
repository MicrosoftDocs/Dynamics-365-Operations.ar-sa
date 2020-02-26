---
title: الوصول إلى العناوين الخاصة حسب دور الأمان
description: يتناول هذا المقال كيفية حل هذه المشكلة والتي يتعذر فيها على العميل الوصول إلى عناوين خاصة.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007982"
---
# <a name="access-to-private-addresses-by-security-role"></a>الوصول إلى العناوين الخاصة حسب دور الأمان

**المشكلة**

بعد تكرار العميل لدور أمان وتسجيل الدخول بهذا الدور الجديد، فلا يمكن للعميل الاطلاع على العناوين التي تم وضع علامة "خاص" عليها.

**‏‏الدقة**

لحل هذه المشكلة، يجب على العميل اتباع الخطوات التالية لدور الأمان المُكرر.

1. انتقل **إدارة المؤسسة \> دفتر العناوين العمومي \> محددات دفتر العناوين العمومية**.
2. في علامة تبويب **أمان الموقع الخاص**، قم بنقل دور الأمان الجديد من قائمة **الأدوار المتاحة** إلى قائمة **الأدوار المُحددة**.
3. حدد **حفظ**.

![صفحة محددات دفتر عناوين عمومي](media/GAD-parameters.png)
