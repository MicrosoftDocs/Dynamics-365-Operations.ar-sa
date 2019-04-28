---
title: ما الجديد أو المتغير في Dynamics 365 for Talent Core HR‏ (1 أكتوبر 2018)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 92f06d29dfa8110106a2a0e71434b2c0c75110b5
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/19/2019
ms.locfileid: "859265"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="8aede-103">ما الجديد أو المتغير في Dynamics 365 for Talent Core HR‏ (8 أكتوبر 2018)</span><span class="sxs-lookup"><span data-stu-id="8aede-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8aede-104">**الإصدار 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="8aede-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="8aede-105">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="8aede-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="8aede-106">السماح باستخدام التواريخ الأخرى على أساس مستوى الإجازة (إدارة الإجازة)</span><span class="sxs-lookup"><span data-stu-id="8aede-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="8aede-107">عند منح إجازات للموظفين، يحدد أساس مستوى منج الإجازات مقدار وقت التوقف الذي تراكم لدى أحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="8aede-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="8aede-108">في الوقت الحالي، تستند هذه المستويات إلى تاريخ بدء عمل الموظف وتاريخ الرتبة.</span><span class="sxs-lookup"><span data-stu-id="8aede-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="8aede-109">في بعض السيناريوهات، يجب أن تستند هذه المستويات إلى تواريخ أخرى وفق حاجة المؤسسات، مثل تاريخ الذكرى السنوية أو تاريخ التوظيف الأصلي.</span><span class="sxs-lookup"><span data-stu-id="8aede-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="8aede-110">تكون هذه التواريخ قيد الاستخدام على خطة الإجازة لتحديد الوقت الذي تحدث فيه الاستحقاقات والقدرة على استخدام هذه التواريخ نفسها عند تسجيل الموظف وإضافته إلى خطة لتحديد مبلغ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="8aede-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="8aede-111">التغييرات الأخرى</span><span class="sxs-lookup"><span data-stu-id="8aede-111">Other changes</span></span>
<span data-ttu-id="8aede-112">تم تضمين إصلاحات متفرقة في هذا الإصدار.</span><span class="sxs-lookup"><span data-stu-id="8aede-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="8aede-113">مشكلات معروفة​</span><span class="sxs-lookup"><span data-stu-id="8aede-113">Known issue</span></span>

<span data-ttu-id="8aede-114">**مشكلة:** عند إضافة مرفق جديد لعامل، تتحول الأزرار **جديد** و **تحرير** إلى اللون الرمادي. **حل بديل:** قبل فتح صفحة المرفق، تأكد أن FactBoxes في صفحة **العامل** مغلق.</span><span class="sxs-lookup"><span data-stu-id="8aede-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="8aede-115">إذا كانت مربعات الحقائق مغلقة عند تحميل صفحة **العامل**، سيتم تمكين زر المرفقات</span><span class="sxs-lookup"><span data-stu-id="8aede-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="8aede-116">(سوف يتم إصلاح هذه المشكلة في التحديث التالي للنظام الأساسي.)</span><span class="sxs-lookup"><span data-stu-id="8aede-116">(This issue will be fixed in the next platform update.)</span></span>
