---
title: ما الجديد أو المتغير في Dynamics 365 Talent (14 فبراير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899210"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a><span data-ttu-id="47bfe-103">ما الجديد أو المتغير في Dynamics 365 Talent (14 فبراير 2019)</span><span class="sxs-lookup"><span data-stu-id="47bfe-103">What's new or changed in Dynamics 365 Talent (February 14, 2019)</span></span>

<span data-ttu-id="47bfe-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Talent.</span><span class="sxs-lookup"><span data-stu-id="47bfe-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="47bfe-105">التغييرات في Attract</span><span class="sxs-lookup"><span data-stu-id="47bfe-105">Changes in Attract</span></span>
<span data-ttu-id="47bfe-106">يتضمن هذا الإصدار إصلاحات أخطاء ثانوية أخرى:</span><span class="sxs-lookup"><span data-stu-id="47bfe-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="47bfe-107">التغييرات في Onboarding</span><span class="sxs-lookup"><span data-stu-id="47bfe-107">Changes in Onboarding</span></span>
<span data-ttu-id="47bfe-108">يتضمن هذا الإصدار إصلاحات أخطاء ثانوية أخرى:</span><span class="sxs-lookup"><span data-stu-id="47bfe-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="47bfe-109">التغييرات في Core HR</span><span class="sxs-lookup"><span data-stu-id="47bfe-109">Changes in Core HR</span></span> 
<span data-ttu-id="47bfe-110">**الإصدار 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="47bfe-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="47bfe-111">لا يصدّر الكيان التعويض الثابت للموظفين جميع السجلات</span><span class="sxs-lookup"><span data-stu-id="47bfe-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="47bfe-112">نتيجة هذا التغيير، يقوم الآن كيان **التعويض الثابت للموظفين** بتصدير جميع السجلات.</span><span class="sxs-lookup"><span data-stu-id="47bfe-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="47bfe-113">ويمكن استخدام الكيان لإنشاء وتحديث سجلات التعويض الثابت الموجودة للموظفين.</span><span class="sxs-lookup"><span data-stu-id="47bfe-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="47bfe-114">لا يراعي تاريخ انتهاء التوظيف إعدادات المنطقة الزمنية المفضلة للموظف</span><span class="sxs-lookup"><span data-stu-id="47bfe-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="47bfe-115">تراعي الآن تواريخ انتهاء التوظيف المنطقة الزمنية المفضلة للمستخدم عند إنشاء أو إنهاء توظيف مع شركة.</span><span class="sxs-lookup"><span data-stu-id="47bfe-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="47bfe-116">تظهر عناوين المملكة المتحدة في صفحة التحليلات كعناوين سويسرية</span><span class="sxs-lookup"><span data-stu-id="47bfe-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="47bfe-117">في هذا الإصدار، تم إجراء تغيير لتصحيح الترتيب الخاطئ في العناوين في التقرير "عدد الموظفين بالموقع" في **إدارة الأفراد**.</span><span class="sxs-lookup"><span data-stu-id="47bfe-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="47bfe-118">عدم تعبئة كود الإنهاء في سجل تعيين منصب العامل‬ عند إنهاء المنصب</span><span class="sxs-lookup"><span data-stu-id="47bfe-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="47bfe-119">تم إجراء تغيير على كود "سبب الإنهاء" الافتراضي عند إنهاء تعيين المناصب للموظفين.</span><span class="sxs-lookup"><span data-stu-id="47bfe-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="47bfe-120">إنشاء كيان جديد لمستويات تعويض الوظيفة</span><span class="sxs-lookup"><span data-stu-id="47bfe-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="47bfe-121">تم إنشاء إطار عمل جديد لإدارة البيانات (DMF).</span><span class="sxs-lookup"><span data-stu-id="47bfe-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="47bfe-122">يوفر الكيان العنصر اللازمة لإنشاء وتحديث مستويات التعويض وقيم السوق ومعلومات الاستطلاع لكل وظيفة معرّفة في النظام.</span><span class="sxs-lookup"><span data-stu-id="47bfe-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
