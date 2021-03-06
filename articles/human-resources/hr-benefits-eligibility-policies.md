---
title: سياسات استحقاق الميزات
description: توفر هذه المقالة معلومات حول سياسات استحقاق الميزات، التي تساعدك على تحديد المؤهلين لميزات معينة.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: cc5dfedc0022cbf9bdbc636bbe96971422c29838
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111303"
---
# <a name="benefit-eligibility-policies"></a>سياسات استحقاق الميزات

توفر هذه المقالة معلومات حول سياسات استحقاق الميزات، التي تساعدك على تحديد المؤهلين لميزات معينة.

عند إنشاء الميزات، تقرر ما الميزات التي ستكون متاحة للموظفين. يعرض الجدول التالي أمثلة للفوائد التي قد توفرها لموظفين محددين.

| الميزة          | الشخص الذي تتوفر له الميزة |
|------------------|---------------------------------|
| التأمين الصحي | كل الموظفين                   |
| الهاتف الجوال     | فريق المبيعات، الموظفون التنفيذيون         |
| مسارات وقوف السيارات   | مديرون تنفيذيون                      |

يتم استخدام المكونات التالية لإنشاء سياسات الاستحقاق:

-   أنواع قاعدة السياسة
-   سياسات استحقاق الميزات

تحدد أنواع قاعدة السياسة معلمات الاستعلام التي تستخدم عندما تقوم بتطوير قواعد نهُج معينة. وبعد إنشاء أنواع قواعد السياسة، يمكنك إنشاء سياسات استحقاق الميزات. وتتيح لك السياسات إنشاء مجموعة من القواعد التي تنطبق على واحد أو أكثر من الكيانات القانونية. وضمن كل سياسة، يمكنك عرض أنواع قاعدة سياسة استحقاق الميزات التي قمت بإنشائها سابقًا. 

وتحدد نطاق القاعدة ضمن السياسة. على سبيل المثال، إذا قمت بإنشاء نوع قاعدة سياسة استحقاق ميزة باسم **المدير التنفيذي**، يمكنك تحديد القاعدة الموجودة في تلك السياسة. في هذا المثال، قد تنص القاعدة على أن أي مسمى وظيفي يحتوي على كلمة "المدير التنفيذي" يجب تضمينه في القاعدة. وبعد أن قمت بتحديد المعلمات الخاصة بالقاعدة أو القواعد المضنة في السياسة، يمكنك تعيين قاعدة محددة للميزة.






[!INCLUDE[footer-include](../includes/footer-banner.md)]